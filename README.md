# @diotoborg/cum-aliquam <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Get the ArrayBuffer out of a DataView, robustly.

This will work in node <= 0.10 and < 0.11.4, where there's no prototype accessor, only a nonconfigurable own property.
It will also work in modern engines where `DataView.prototype.buffer` has been deleted after this module has loaded.

## Example

```js
const dataViewBuffer = require('@diotoborg/cum-aliquam');
const assert = require('assert');

const ab = new ArrayBuffer(0);
const dv = new DataView(ab);
assert.equal(dataViewBuffer(dv), ab);
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@diotoborg/cum-aliquam
[npm-version-svg]: https://versionbadg.es/inspect-js/@diotoborg/cum-aliquam.svg
[deps-svg]: https://david-dm.org/inspect-js/@diotoborg/cum-aliquam.svg
[deps-url]: https://david-dm.org/inspect-js/@diotoborg/cum-aliquam
[dev-deps-svg]: https://david-dm.org/inspect-js/@diotoborg/cum-aliquam/dev-status.svg
[dev-deps-url]: https://david-dm.org/inspect-js/@diotoborg/cum-aliquam#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@diotoborg/cum-aliquam.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@diotoborg/cum-aliquam.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@diotoborg/cum-aliquam.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@diotoborg/cum-aliquam
[codecov-image]: https://codecov.io/gh/inspect-js/@diotoborg/cum-aliquam/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/inspect-js/@diotoborg/cum-aliquam/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/inspect-js/@diotoborg/cum-aliquam
[actions-url]: https://github.com/inspect-js/@diotoborg/cum-aliquam/actions
