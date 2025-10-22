# Echo

This is a monorepo app, we build it using
* pnpm
* turborepo
* next.js
* tailwind
* schadcn/ui (2.9.2) + turborepo template

## Monorepo
* Each app in apps has it's own package.json and each package under packages has its own package.json
* All the projects use the same tsconfig.json, typescript configs
* All the projects will be run separately but they use the same packages, they are deployed separately as well.

## Development
* To start local servers for the apps we use command `turbo dev`
* All the apps will get their own ports to run the application
* 

## Creating internal package
* Follow steps here [here](https://turborepo.com/docs/crafting-your-repository/creating-an-internal-package)
* As we are using schadcn/ui we need to replace @repo in package.json to @workspace as this template uses @workspace as alias.
* When `turbo dev` is run we will see a dev server for the math package because we have add `dev` script in math package.json
* Like above `turbo build` will build the package because we have `build` script in package.json.