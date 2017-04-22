# npmdoc-husky

#### api documentation for  [husky (v0.13.3)](https://github.com/typicode/husky)  [![npm package](https://img.shields.io/npm/v/npmdoc-husky.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-husky) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-husky.svg)](https://travis-ci.org/npmdoc/node-npmdoc-husky)

#### Prevents bad commit or push (git hooks, pre-commit/precommit, pre-push/prepush, post-merge/postmerge and all that stuff...)

[![NPM](https://nodei.co/npm/husky.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/husky)

- [https://npmdoc.github.io/node-npmdoc-husky/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-husky/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-husky/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-husky/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-husky/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-husky/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Typicode"
    },
    "bugs": {
        "url": "https://github.com/typicode/husky/issues"
    },
    "dependencies": {
        "chalk": "^1.1.3",
        "find-parent-dir": "^0.3.0",
        "is-ci": "^1.0.9",
        "normalize-path": "^1.0.0"
    },
    "description": "Prevents bad commit or push (git hooks, pre-commit/precommit, pre-push/prepush, post-merge/postmerge and all that stuff...)",
    "devDependencies": {
        "expect": "^1.20.2",
        "mocha": "^3.2.0",
        "mock-fs": "^3.12.1",
        "pkg-ok": "^1.0.1",
        "rimraf": "^2.2.8",
        "standard": "^8.6.0"
    },
    "directories": {},
    "dist": {
        "shasum": "bc2066080badc8b8fe3516e881f5bc68a57052ff",
        "tarball": "https://registry.npmjs.org/husky/-/husky-0.13.3.tgz"
    },
    "gitHead": "4b5011e854c0bccf384805107233bc72db77d9a8",
    "homepage": "https://github.com/typicode/husky",
    "keywords": [
        "git",
        "hook",
        "hooks",
        "pre-commit",
        "precommit",
        "post-commit",
        "postcommit",
        "pre-push",
        "prepush",
        "post-merge",
        "postmerge",
        "test"
    ],
    "license": "MIT",
    "main": "./src/index.js",
    "maintainers": [
        {
            "name": "typicode"
        }
    ],
    "name": "husky",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/typicode/husky.git"
    },
    "scripts": {
        "install": "node ./bin/install.js",
        "precommit": "npm test",
        "prepublish": "pkg-ok",
        "test": "mocha && standard",
        "uninstall": "node ./bin/uninstall.js"
    },
    "standard": {
        "env": {
            "mocha": true
        }
    },
    "version": "0.13.3",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
