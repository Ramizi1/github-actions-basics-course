# tsconfig

> Shared [TypeScript config](https://www.typescriptlang.org/docs/handbook/tsconfig-json.html) for my projects

## Install

```bash
yarn add -DE @Ramizi1/tsconfig
```

### Install Via GitHub NPM Packages

You can install this package from the GitHub NPM Package Repository. In order to do this, you must first authenticate with GitHub packages. You can read more about this process here: [GitHub - Installing A GitHub Package](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-npm-registry#installing-a-package).

```bash
yarn config set @lookio:registry https://npm.pkg.github.com/
echo "//npm.pkg.github.com/:_authToken=<github_personal_access_token>" > .npmrc
yarn add -DE @Ramizi1/tsconfig
```

## Usage

`tsconfig.json`

```json
{
  "extends": "@Ramizi1/tsconfig/tsconfig.json",
  "compilerOptions": {
    "outDir": "dist"
  },
  "include": [
    "**/*.ts"
  ]
}
```

When you are targeting a higher version of Node.js, check the relevant ECMAScript version and add it as `target`:

```json
{
  "extends": "@Ramizi1/tsconfig/tsconfig.json",
  "compilerOptions": {
    "outDir": "dist",
    "target": "ES2021"
  },
  "include": [
    "**/*.ts"
  ]
}
```

When you are building a NPM package:

```json
{
  "extends": "@Ramizi1/tsconfig",
  "compilerOptions": {
    "outDir": "dist",
    "declaration": true
  },
  "include": [
    "**/*.ts"
  ]
}
```

## Publish New Version

```bash
# Authenticate with NPM Package Registry
npm login

# Run publish script
yarn publish:npm
yarn publish:github
```

---

## Shared Configurations

- @Ramizi1/eslint-config: [eslint-config](https://github.com/Ramizi1/eslint-config)
- @Ramizi1/tsconfig: [tsconfig](https://github.com/Ramizi1/tsconfig)
- @Ramizi1/prettier-config: [prettier-config](https://github.com/Ramizi1/prettier-config)
