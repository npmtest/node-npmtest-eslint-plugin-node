# npmtest-eslint-plugin-node

#### basic test coverage for  [eslint-plugin-node (v4.2.2)](https://github.com/mysticatea/eslint-plugin-node#readme)  [![npm package](https://img.shields.io/npm/v/npmtest-eslint-plugin-node.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-eslint-plugin-node) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-eslint-plugin-node.svg)](https://travis-ci.org/npmtest/node-npmtest-eslint-plugin-node)

#### Additional ESLint's rules for Node.js

[![NPM](https://nodei.co/npm/eslint-plugin-node.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/eslint-plugin-node)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-eslint-plugin-node/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-eslint-plugin-node/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-eslint-plugin-node/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-eslint-plugin-node/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-eslint-plugin-node/build/test-report.html)|
| test-server-github : | [![github.com test-server](https://npmtest.github.io/node-npmtest-eslint-plugin-node/GitHub-Mark-32px.png)](https://npmtest.github.io/node-npmtest-eslint-plugin-node/build/app/index.html) | | build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-eslint-plugin-node/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-eslint-plugin-node/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-eslint-plugin-node/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-eslint-plugin-node/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-eslint-plugin-node/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-eslint-plugin-node/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-eslint-plugin-node/build/test-report.html](https://npmtest.github.io/node-npmtest-eslint-plugin-node/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-eslint-plugin-node/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-eslint-plugin-node/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-eslint-plugin-node/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-eslint-plugin-node/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-eslint-plugin-node/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-eslint-plugin-node/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-eslint-plugin-node/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-eslint-plugin-node/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Toru Nagashima"
    },
    "bugs": {
        "url": "https://github.com/mysticatea/eslint-plugin-node/issues"
    },
    "dependencies": {
        "ignore": "^3.0.11",
        "minimatch": "^3.0.2",
        "object-assign": "^4.0.1",
        "resolve": "^1.1.7",
        "semver": "5.3.0"
    },
    "description": "Additional ESLint's rules for Node.js",
    "devDependencies": {
        "@types/minimatch": "^2.0.29",
        "@types/node": "^4.2.1",
        "@types/resolve": "0.0.4",
        "@types/semver": "^5.3.30",
        "codecov": "^1.0.1",
        "eslint": "^3.9.0",
        "eslint-config-mysticatea": "^7.0.0",
        "mocha": "^3.0.2",
        "nyc": "^8.3.0",
        "opener": "^1.4.2",
        "rimraf": "^2.4.4",
        "shelljs": "^0.7.0"
    },
    "directories": {},
    "dist": {
        "shasum": "82959ca9aed79fcbd28bb1b188d05cac04fb3363",
        "tarball": "https://registry.npmjs.org/eslint-plugin-node/-/eslint-plugin-node-4.2.2.tgz"
    },
    "engines": {
        "node": ">=4"
    },
    "files": [
        "conf",
        "lib",
        "index.js"
    ],
    "gitHead": "f1a137b1250cd457cd9dfdf0bf851d1efa0ce2fa",
    "homepage": "https://github.com/mysticatea/eslint-plugin-node#readme",
    "keywords": [
        "eslint",
        "eslintplugin",
        "eslint-plugin",
        "node",
        "nodejs",
        "ecmascript",
        "shebang",
        "file",
        "path",
        "import",
        "require"
    ],
    "license": "MIT",
    "maintainers": [
        {
            "name": "mysticatea"
        }
    ],
    "name": "eslint-plugin-node",
    "optionalDependencies": {},
    "peerDependencies": {
        "eslint": ">=3.1.0"
    },
    "repository": {
        "type": "git",
        "url": "git+https://github.com/mysticatea/eslint-plugin-node.git"
    },
    "scripts": {
        "build": "node scripts/generate-index.js",
        "clean": "rimraf .nyc_output coverage index.js",
        "codecov": "nyc report -r lcovonly && codecov",
        "coverage": "nyc report -r lcov && opener ./coverage/lcov-report/index.html",
        "lint": "eslint lib tests/lib index.js",
        "postversion": "git push && git push --tags",
        "pretest": "npm run -s lint",
        "preversion": "npm t && npm run build",
        "test": "nyc npm run -s test:_mocha",
        "test:_mocha": "_mocha tests/lib/**/*.js --reporter progress",
        "watch": "npm run test:_mocha -- --watch --growl"
    },
    "version": "4.2.2",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
