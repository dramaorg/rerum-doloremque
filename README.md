# @dramaorg/rerum-doloremque <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Get the ArrayBuffer out of a TypedArray, robustly.

This will work in node <= 0.10 and < 0.11.4, where there's no prototype accessor, only a nonconfigurable own property.
It will also work in modern engines where `TypedArray.prototype.buffer` has been deleted after this module has loaded.

## Example

```js
const typedArrayBuffer = require('@dramaorg/rerum-doloremque');
const assert = require('assert');

const arr = new Uint8Array(0);
assert.equal(arr.buffer, typedArrayBuffer(arr));
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@dramaorg/rerum-doloremque
[npm-version-svg]: https://versionbadg.es/inspect-js/@dramaorg/rerum-doloremque.svg
[deps-svg]: https://david-dm.org/inspect-js/@dramaorg/rerum-doloremque.svg
[deps-url]: https://david-dm.org/inspect-js/@dramaorg/rerum-doloremque
[dev-deps-svg]: https://david-dm.org/inspect-js/@dramaorg/rerum-doloremque/dev-status.svg
[dev-deps-url]: https://david-dm.org/inspect-js/@dramaorg/rerum-doloremque#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@dramaorg/rerum-doloremque.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@dramaorg/rerum-doloremque.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@dramaorg/rerum-doloremque.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@dramaorg/rerum-doloremque
[codecov-image]: https://codecov.io/gh/inspect-js/@dramaorg/rerum-doloremque/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/inspect-js/@dramaorg/rerum-doloremque/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/inspect-js/@dramaorg/rerum-doloremque
[actions-url]: https://github.com/inspect-js/@dramaorg/rerum-doloremque/actions
