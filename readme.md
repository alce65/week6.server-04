# Backend Node: TS - Eslint -Jest

## Setup

- npm init
- git init
- .editorconfig
- .gitignore
- TS

  ```shell
  npm i -D typescript @types/node
  ```

tsconfig

  ```shell
  npx tsc --init
  ```

ESModule Config: package.json

```json
  "type": "module"
```



- ESLint

```shell
npx eslint --init
npm i -D eslint-config-prettier
```

Eslint config

```json
{
  "env": {
    "browser": true,
    "es2021": true,
    "node": true,
    "jest": true
  },
  "extends": ["xo", "prettier"],
  "parser": "@typescript-eslint/parser",
  "parserOptions": {
    "ecmaVersion": 12,
    "sourceType": "module"
  },
  "plugins": ["@typescript-eslint"],
  "rules": {}
}
```

Prettier config: package.json

```json
  "prettier": {
    "singleQuote": true
  }
```


- Jest

```shell
npm i -D jest ts-jest @types/jest jest-ts-webcompat-resolver
```

jest config

```js
/** @type {import('ts-jest').JestConfigWithTsJest} */
export default {
  preset: 'ts-jest',
  testEnvironment: 'node',
  testPathIgnorePatterns: ['dist'],
  resolver: 'jest-ts-webcompat-resolver',
  collectCoverageFrom: ['src/**/*.ts'],
  coveragePathIgnorePatterns: ['index.ts'],
};
```
