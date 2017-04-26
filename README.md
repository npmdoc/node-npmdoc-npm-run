# npmdoc-npm-run

#### basic api documentation for  [npm-run (v4.1.2)](https://github.com/timoxley/npm-run)  [![npm package](https://img.shields.io/npm/v/npmdoc-npm-run.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-npm-run) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-npm-run.svg)](https://travis-ci.org/npmdoc/node-npmdoc-npm-run)

#### Run executables for locally-installed packages without using ./node_modules/.bin

[![NPM](https://nodei.co/npm/npm-run.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/npm-run)

- [https://npmdoc.github.io/node-npmdoc-npm-run/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-npm-run/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-npm-run/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-npm-run/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-npm-run/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-npm-run/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Tim Oxley"
    },
    "bin": {
        "npm-run": "bin/npm-run.js"
    },
    "bugs": {
        "url": "https://github.com/timoxley/npm-run/issues"
    },
    "dependencies": {
        "cross-spawn": "^5.1.0",
        "minimist": "^1.2.0",
        "npm-path": "^2.0.3",
        "npm-which": "^3.0.1",
        "serializerr": "^1.0.3",
        "sync-exec": "^0.6.2"
    },
    "description": "Run executables for locally-installed packages without using ./node_modules/.bin",
    "devDependencies": {
        "bl": "^1.2.0",
        "standard": "^9.0.0",
        "tape": "^4.6.3"
    },
    "directories": {
        "test": "test"
    },
    "dist": {
        "shasum": "1030e1ec56908c89fcc3fa366d03a2c2ba98eb99",
        "tarball": "https://registry.npmjs.org/npm-run/-/npm-run-4.1.2.tgz"
    },
    "engines": {
        "node": ">=4.2.0"
    },
    "gitHead": "80a842e1509b8faaefaca65f06a8c23c2c971a2b",
    "homepage": "https://github.com/timoxley/npm-run",
    "keywords": [
        "npm",
        "path",
        "executable",
        ".bin",
        "run"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "timoxley"
        }
    ],
    "name": "npm-run",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/timoxley/npm-run.git"
    },
    "scripts": {
        "lint": "standard",
        "test": "tape test/*.js && npm run lint"
    },
    "version": "4.1.2"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
