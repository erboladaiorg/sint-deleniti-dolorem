# @erboladaiorg/sint-deleniti-dolorem <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Is this value a JS WeakMap? This module works cross-realm/iframe, and despite ES6 @@toStringTag.

## Example

```js
var isWeakMap = require('@erboladaiorg/sint-deleniti-dolorem');
assert(!isWeakMap(function () {}));
assert(!isWeakMap(null));
assert(!isWeakMap(function* () { yield 42; return Infinity; });
assert(!isWeakMap(Symbol('foo')));
assert(!isWeakMap(1n));
assert(!isWeakMap(Object(1n)));

assert(!isWeakMap(new Set()));
assert(!isWeakMap(new WeakSet()));
assert(!isWeakMap(new Map()));

assert(isWeakMap(new WeakMap()));

class MyWeakMap extends WeakMap {}
assert(isWeakMap(new MyWeakMap()));
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@erboladaiorg/sint-deleniti-dolorem
[npm-version-svg]: https://versionbadg.es/inspect-js/@erboladaiorg/sint-deleniti-dolorem.svg
[deps-svg]: https://david-dm.org/inspect-js/@erboladaiorg/sint-deleniti-dolorem.svg
[deps-url]: https://david-dm.org/inspect-js/@erboladaiorg/sint-deleniti-dolorem
[dev-deps-svg]: https://david-dm.org/inspect-js/@erboladaiorg/sint-deleniti-dolorem/dev-status.svg
[dev-deps-url]: https://david-dm.org/inspect-js/@erboladaiorg/sint-deleniti-dolorem#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@erboladaiorg/sint-deleniti-dolorem.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@erboladaiorg/sint-deleniti-dolorem.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@erboladaiorg/sint-deleniti-dolorem.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@erboladaiorg/sint-deleniti-dolorem
[codecov-image]: https://codecov.io/gh/inspect-js/@erboladaiorg/sint-deleniti-dolorem/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/inspect-js/@erboladaiorg/sint-deleniti-dolorem/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/inspect-js/@erboladaiorg/sint-deleniti-dolorem
[actions-url]: https://github.com/erboladaiorg/sint-deleniti-dolorem/actions
