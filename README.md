# npmdoc-yargs

#### api documentation for  [yargs (v7.1.0)](http://yargs.js.org/)  [![npm package](https://img.shields.io/npm/v/npmdoc-yargs.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-yargs) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-yargs.svg)](https://travis-ci.org/npmdoc/node-npmdoc-yargs)

#### yargs the modern, pirate-themed, successor to optimist.

[![NPM](https://nodei.co/npm/yargs.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/yargs)

- [https://npmdoc.github.io/node-npmdoc-yargs/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-yargs/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-yargs/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-yargs/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-yargs/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-yargs/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "yargs",
    "version": "7.1.0",
    "description": "yargs the modern, pirate-themed, successor to optimist.",
    "main": "./index.js",
    "files": [
        "index.js",
        "yargs.js",
        "lib",
        "locales",
        "completion.sh.hbs",
        "LICENSE"
    ],
    "dependencies": {
        "camelcase": "^3.0.0",
        "cliui": "^3.2.0",
        "decamelize": "^1.1.1",
        "get-caller-file": "^1.0.1",
        "os-locale": "^1.4.0",
        "read-pkg-up": "^1.0.1",
        "require-directory": "^2.1.1",
        "require-main-filename": "^1.0.1",
        "set-blocking": "^2.0.0",
        "string-width": "^1.0.2",
        "which-module": "^1.0.0",
        "y18n": "^3.2.1",
        "yargs-parser": "^5.0.0"
    },
    "devDependencies": {
        "chai": "^3.4.1",
        "chalk": "^1.1.3",
        "coveralls": "^2.11.11",
        "cpr": "^2.0.0",
        "cross-spawn": "^5.0.1",
        "es6-promise": "^4.0.2",
        "hashish": "0.0.4",
        "mocha": "^3.0.1",
        "nyc": "^10.0.0",
        "rimraf": "^2.5.0",
        "standard": "^8.6.0",
        "standard-version": "^3.0.0",
        "which": "^1.2.9"
    },
    "scripts": {
        "pretest": "standard",
        "test": "nyc --cache mocha --require ./test/before.js --timeout=8000 --check-leaks",
        "coverage": "nyc report --reporter=text-lcov | coveralls",
        "release": "standard-version"
    },
    "repository": {
        "type": "git",
        "url": "http://github.com/yargs/yargs.git"
    },
    "homepage": "http://yargs.js.org/",
    "standard": {
        "ignore": [
            "**/example/**"
        ]
    },
    "keywords": [
        "argument",
        "args",
        "option",
        "parser",
        "parsing",
        "cli",
        "command"
    ],
    "license": "MIT",
    "engine": {
        "node": ">=0.10"
    },
    "greenkeeper": {
        "ignore": [
            "string-width",
            "read-pkg-up",
            "camelcase"
        ]
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
