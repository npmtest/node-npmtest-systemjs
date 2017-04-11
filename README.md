# test coverage for  [systemjs (v0.20.12)](https://github.com/systemjs/systemjs#readme)  [![npm package](https://img.shields.io/npm/v/npmtest-systemjs.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-systemjs) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-systemjs.svg)](https://travis-ci.org/npmtest/node-npmtest-systemjs)
#### Dynamic ES module loader

[![NPM](https://nodei.co/npm/systemjs.png?downloads=true)](https://www.npmjs.com/package/systemjs)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-systemjs/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-systemjs/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-systemjs/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-systemjs/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-systemjs/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-systemjs/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-systemjs/tree/gh-pages/build)|

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-systemjs/build/screenCapture.buildCustomOrg.browser.coverage.html.png)](https://npmtest.github.io/node-npmtest-systemjs/build/coverage.html/index.html)

[![test-report](https://npmtest.github.io/node-npmtest-systemjs/build/screenCapture.buildCustomOrg.browser.%252Fhome%252Ftravis%252Fbuild%252Fnpmtest%252Fnode-npmtest-systemjs%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-systemjs/build/test-report.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-systemjs/build/screenCapture.buildApidoc.browser.%252Fhome%252Ftravis%252Fbuild%252Fnpmdoc%252Fnode-npmdoc-systemjs%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-systemjs/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-systemjs/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-systemjs/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Guy Bedford"
    },
    "bugs": {
        "url": "https://github.com/systemjs/systemjs/issues"
    },
    "dependencies": {},
    "description": "Dynamic ES module loader",
    "devDependencies": {
        "babel-core": "^6.21.0",
        "babel-plugin-syntax-dynamic-import": "^6.18.0",
        "babel-plugin-transform-es2015-modules-systemjs": "^6.19.0",
        "bluebird": "^3.4.6",
        "es-module-loader": "^2.1.5",
        "mocha": "^3.1.2",
        "plugin-typescript": "^5.2.7",
        "rollup": "^0.41.1",
        "rollup-plugin-node-resolve": "^2.0.0",
        "rollup-plugin-replace": "^1.1.1",
        "systemjs-plugin-babel": "0.0.17",
        "systemjs-plugin-traceur": "0.0.3",
        "traceur": "0.0.111",
        "typescript": "^2.0.6",
        "uglifyjs": "^2.4.10"
    },
    "directories": {},
    "dist": {
        "shasum": "135cc471280448453347829ebb9639a09a67f101",
        "tarball": "https://registry.npmjs.org/systemjs/-/systemjs-0.20.12.tgz"
    },
    "files": [
        "dist"
    ],
    "gitHead": "c484f143c552a5c5aba875b2089c21a733d50ca6",
    "homepage": "https://github.com/systemjs/systemjs#readme",
    "license": "MIT",
    "main": "dist/system.src.js",
    "maintainers": [
        {
            "name": "guybedford",
            "email": "guybedford@gmail.com"
        }
    ],
    "name": "systemjs",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/systemjs/systemjs.git"
    },
    "scripts": {
        "build": "npm run build:dev && npm run build:production",
        "build:dev": "rollup -c",
        "build:production": "rollup -c --environment production",
        "footprint": "npm run footprint:dev && npm run footprint:production",
        "footprint:dev": "uglifyjs dist/system.src.js -cm --screw-ie8 | gzip -9f | wc -c",
        "footprint:production": "uglifyjs dist/system-production.src.js -cm --screw-ie8 | gzip -9f | wc -c",
        "irhydra": "node --trace-hydrogen --trace-phase=Z --trace-deopt --code-comments --hydrogen-track-positions --redirect-code-traces --redirect-code-traces-to=code.asm --print-opt-code --trace_hydrogen_file=hydrogen.cfg irhydra/load.js",
        "min": "npm run min:dev && npm run min:production",
        "min:dev": "cd dist && uglifyjs system.src.js -cm --in-source-map system.src.js.map --source-map system.js.map --screw-ie8 --comments '/SystemJS v/' > system.js",
        "min:production": "cd dist && uglifyjs system-production.src.js -cm --in-source-map system-production.src.js.map --source-map system-production.js.map --screw-ie8 --comments '/SystemJS v/' > system-production.js",
        "prepublish": "rm -r dist && npm run build && npm run min",
        "test": "npm run test:production && npm run test:babel && npm run test:traceur && npm run test:typescript",
        "test:babel": "mocha test/test-babel.js -u tdd --reporter dot",
        "test:production": "mocha test/test-production.js -u tdd --reporter dot",
        "test:traceur": "mocha test/test-traceur.js -u tdd --reporter dot",
        "test:typescript": "mocha test/test-typescript.js -u tdd --reporter dot"
    },
    "version": "0.20.12"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
