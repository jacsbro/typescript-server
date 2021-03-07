# Minimal TypeScript project setup for a Node.js project

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This repository contains a simple setup for a Node.js project with TypeScript. It has been forked from 
[here](https://github.com/bobaekang/minimal-typescript-setup) and just tweaked a bit. 

Please refer to [this blog post](https://bobaekang.com/blog/minimal-typescript-project-setup-for-curious-minds/) for 
the original authors detailed explanation. This is the list of my modifications to the original:

- add a ``.gitignore``
- add [nodemon](https://www.npmjs.com/package/nodemon) and the necessary configuration

## Project setup

```shell
git clone https://github.com/jacsbro/typescript-server.git
cd typescript-server

npm install
npm run start:watch
```

## Use as start for a new local project

```shell
curl -L https://github.com/jacsbro/typescript-server/archive/master.zip -o ts.zip
unzip ts.zip && mv typescript-server-master <new-project-name> && rm ts.zip
cd <new-project-name> && rm LICENSE README.md
```

## Project structure

```
/
/dist   <- compiled JavaScript code goes here
/src    <- TypeScript source code lives here
/test   <- test files (**.test.ts) live     here
```

## Main dependencies

* [TypeScript](https://www.typescriptlang.org/)
* [`ts-node`](https://github.com/TypeStrong/ts-node) for development server
* [ESLint](https://eslint.org/) for linting
* [`typescript-eslint`](https://github.com/typescript-eslint/typescript-eslint) for ESLint plugins to support TypeScript
* [Prettier](https://prettier.io/) for formatting source code
* [Mocha](https://mochajs.org/) for testing
* [Nodemon](https://www.npmjs.com/package/nodemon) for hot reload
## npm scripts

npm script | description
--- | ---
`build` | Compile TypeScript source code to JavaScript
`lint` | Typecheck, lint and format TypeScript source code
`serve` | Run TypeScript source code directly with `ts-node`
`start:watch` | Run changed JavaScript code
`test` | Run tests with Mocha

## License

[MIT](./LICENSE)
