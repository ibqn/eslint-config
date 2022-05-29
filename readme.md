## Shared common eslint config

This package is published on `npmjs` and as well as on `github` registries.

To be able to install this package from the `github` registry add the following line to your `~/.npmrc` file

```text
@ibqn:registry=https://npm.pkg.github.com
```

To include this eslint configuration add the following to your `package.json` file

```json
"eslintConfig": {
    "extends": "@ibqn/eslint-config"
  },
```

additionally add the following commands to your script

```json
"scripts": {
  ...
  "lint": "eslint . --ext .ts",
  "lint:fix": "pnpm run lint -- --fix",
  ...
}
```

and install the following peer dependencies

```json
"@typescript-eslint/eslint-plugin": "^5.26.0",
"@typescript-eslint/parser": "^5.26.0",
"eslint": "^8.16.0",
"eslint-config-prettier": "^8.5.0",
```
