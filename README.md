# api documentation for  [husky (v0.13.3)](https://github.com/typicode/husky)  [![npm package](https://img.shields.io/npm/v/npmdoc-husky.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-husky) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-husky.svg)](https://travis-ci.org/npmdoc/node-npmdoc-husky)
#### Prevents bad commit or push (git hooks, pre-commit/precommit, pre-push/prepush, post-merge/postmerge and all that stuff...)

[![NPM](https://nodei.co/npm/husky.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/husky)

[![apidoc](https://npmdoc.github.io/node-npmdoc-husky/build/screenCapture.buildCi.browser.apidoc.html.png)](https://npmdoc.github.io/node-npmdoc-husky/build/apidoc.html)

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
    "version": "0.13.3"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module husky](#apidoc.module.husky)
1.  [function <span class="apidocSignatureSpan">husky.</span>installFrom (huskyDir)](#apidoc.element.husky.installFrom)
1.  [function <span class="apidocSignatureSpan">husky.</span>uninstallFrom (huskyDir)](#apidoc.element.husky.uninstallFrom)



# <a name="apidoc.module.husky"></a>[module husky](#apidoc.module.husky)

#### <a name="apidoc.element.husky.installFrom"></a>[function <span class="apidocSignatureSpan">husky.</span>installFrom (huskyDir)](#apidoc.element.husky.installFrom)
- description and source-code
```javascript
function installFrom(huskyDir) {
  try {
    var isInSubNodeModule = (huskyDir.match(/node_modules/g) || []).length > 1
    if (isInSubNodeModule) {
      return console.log(
        'Trying to install from sub \'node_module\' directory,',
        'skipping Git hooks installation'
      )
    }

    var hooksDir = findHooksDir(huskyDir)

    if (hooksDir) {
      hooks.forEach(function (hookName) {
        var npmScriptName = hookName.replace(/-/g, '')
        createHook(huskyDir, hooksDir, hookName, npmScriptName)
      })
      console.log('done\n')
    } else {
      console.log('Can\'t find .git directory, skipping Git hooks installation')
    }
  } catch (e) {
    console.error(e)
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.husky.uninstallFrom"></a>[function <span class="apidocSignatureSpan">husky.</span>uninstallFrom (huskyDir)](#apidoc.element.husky.uninstallFrom)
- description and source-code
```javascript
function uninstallFrom(huskyDir) {
  try {
    var hooksDir = findHooksDir(huskyDir)

    hooks.forEach(function (hookName) {
      removeHook(hooksDir, hookName)
    })
    console.log('done\n')
  } catch (e) {
    console.error(e)
  }
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
