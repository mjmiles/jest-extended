<div align="center">
  <h1>jest-extended</h1>

  🃏💪

  Additional Jest matchers
</div>

<hr />

[![Build Status](https://img.shields.io/travis/mattphillips/jest-extended.svg?style=flat-square)](https://travis-ci.org/mattphillips/jest-extended)
[![Code Coverage](https://img.shields.io/codecov/c/github/mattphillips/jest-extended.svg?style=flat-square)](https://codecov.io/github/mattphillips/jest-extended)
[![version](https://img.shields.io/npm/v/jest-extended.svg?style=flat-square)](https://www.npmjs.com/package/jest-extended)
[![downloads](https://img.shields.io/npm/dm/jest-extended.svg?style=flat-square)](http://npm-stat.com/charts.html?package=jest-extended&from=2017-09-14)
[![MIT License](https://img.shields.io/npm/l/jest-extended.svg?style=flat-square)](https://github.com/mattphillips/jest-extended/blob/master/LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)
[![Roadmap](https://img.shields.io/badge/%F0%9F%93%94-roadmap-CD9523.svg?style=flat-square)](https://github.com/mattphillips/jest-extended/blob/master/docs/ROADMAP.md)
[![Examples](https://img.shields.io/badge/%F0%9F%92%A1-examples-ff615b.svg?style=flat-square)](https://github.com/mattphillips/jest-extended/blob/master/docs/EXAMPLES.md)

## Problem

Jest is an amazing test running and has some awesome assertion APIs built in by default. However there are times when
having more specific matchers (assertions) would be far more convenient.

## Solution

jest-extended aims to add additional matchers to Jest's default ones making it easy to test everything 🙌

## Contributing

If you've come here to help contribute - Thanks! Take a look at the [contributing](/CONTRIBUTING.md) docs as a way of getting started.

---

- [Installation](#installation)
- [Setup](#setup)
- [API](#api)
  * [.toBeTrue()](#tobetrue)
  * [.toBeFalse()](#tobefalse)
  * [.pass(message)](#passmessage)
  * [.fail(message)](#failmessage)
  * [.toBeNil()](#tobenil)
  * [.toBeNaN()](#tobenan)
  * [.toBeEmpty()](#tobeempty)
  * [.toBeWithin(start, end)](#tobewithinstart-end)
  * [.toContainKey(key)](#tocontainkeykey)
  * [.toContainKeys([keys])](#tocontainkeyskeys)
  * [.toContainAllKeys([keys])](#tocontainallkeyskeys)
  * [.toContainAnyKeys([keys])](#tocontainanykeyskeys)
  * [.toContainValue(value)](#tocontainvaluevalue)
  * [.toContainValues([values])](#tocontainvaluesvalues)
  * [.toContainAllValues([values])](#tocontainallvaluesvalues)
  * [.toContainAnyValues([values])](#tocontainanyvaluesvalues)
  * [.toContainEntry([key, value])](#tocontainentrykey-value)
  * [.toContainEntries([[key, value]])](#tocontainentrieskey-value)
  * [.toContainAllEntries([[key, value]])](#tocontainallentrieskey-value)
  * [.toContainAnyEntries([[key, value]])](#tocontainanyentrieskey-value)
  * [.toSatisfy(predicate)](#tosatisfypredicate)
  * [.toHaveAllMembers([members])](#tohaveallmembersmembers)
  * [.toHaveSomeMembers([members])](#tohavesomemembersmembers)
  * [.toBeOneOf([members])](#tobeoneofmembers)
  * [.toBeExtensible()](#tobeextensible)
  * [.toBeSealed()](#tobesealed)
  * [.toBeFrozen()](#tobefrozen)
  * [.toBeFinite()](#tobefinite)
  * [.toBePositive()](#tobepositive)
  * [.toBeNegative()](#tobenegative)
  * [.toBeEven()](#tobeeven)
  * [.toBeOdd()](#tobeodd)
  * [.toBeFunction()](#tobefunction)
  * [.toBeObject()](#tobeobject)
  * [.toBeArray()](#tobearray)
  * [.toBeString()](#tobestring)
  * [.toBeNumber()](#tobenumber)
  * [.toBeBoolean()](#tobeboolean)
  * [.toStartWith(prefix)](#tostartwithprefix)
  * [.toEndWith(suffix)](#toendwithsuffix)
  * [.toInclude(substring)](#toincludesubstring)
  * [.toIncludeRepeated(substring, times)](#toincluderepeatedsubstring-times)
  * [.toIncludeMultiple([substring])](#toincludemultiplesubstring)
  * [.toEqualCaseInsensitive(string)](#toequalcaseinsensitivestring)
- [Contributors](#contributors)
- [LICENSE](#license)

## Installation

With npm:
```sh
npm install --save-dev jest-extended
```

With yarn:
```sh
yarn add -D jest-extended
```

## Setup

Add jest-extended to your Jest setupTestFrameworkScriptFile configuration. [See for help](http://facebook.github.io/jest/docs/en/configuration.html#setuptestframeworkscriptfile-string)

``` json
"jest": {
  "setupTestFrameworkScriptFile": "jest-extended"
}
```

## API

### .toBeTrue()

Use `.toBeTrue` when checking a value is equal (===) to `true`.

```js
test('is jest cool', () => {
  expect(isJestCool()).toBeTrue();
  expect(false).not.toBeTrue();
});
```

### .toBeFalse()

_Note: Currently unimplemented_

Use `.toBeFalse` when checking a value is equal (===) to `false`.

```js
test('returns false', () => {
  expect(areWeThereYet()).toBeFalse();
  expect(true).not.toBeFalse();
});
```

### .pass(message)

_Note: Currently unimplemented_

Passing assertion.

```js
expect().pass('should pass');
```

### .fail(message)

_Note: Currently unimplemented_

Failing assertion.

```js
expect().fail('test should fail');
```

### .toBeNil()

_Note: Currently unimplemented_

Use `.toBeNil` when checking a value is `null` or `undefined`.

```js
test('passes when value is null or undefined', () => {
  expect(null).toBeNil();
  expect(undefined).toBeNil();
  expect(true).not.toBeNil();
});
```

### .toBeNaN()

_Note: Currently unimplemented_

Use `.toBeNaN` when checking a value is `NaN`.

```js
test('passes when value is NaN', () => {
  expect(NaN).toBeNaN();
  expect(1).not.toBeNaN();
});
```

### .toBeEmpty()

_Note: Currently unimplemented_

Use `.toBeEmpty` when checking if a `String` `''`, `Array` `[]` or `Object` `{}` is empty.

```js
test('passes when given an empty string', () => {
  expect('').toBeEmpty();
  expect('hello').not.toBeEmpty();
});

test('passes when given an empty array', () => {
  expect([]).toBeEmpty();
  expect(['hello']).not.toBeEmpty();
});

test('passes when given an empty object', () => {
  expect({}).toBeEmpty();
  expect({ hello: 'world' }).not.toBeEmpty();
});
```

### .toBeWithin(start, end)

Use `.toBeWithin` when checking if a number is in between the given bounds of: start (inclusive) and end (exclusive).

```js
test('passes when number is within given bounds', () => {
  expect(1).toBeWithin(1, 3);
  expect(2).toBeWithin(1, 3);
  expect(3).not.toBeWithin(1, 3);
});
```

### .toContainKey(key)

Use `.toContainKey` when checking if an object contains the provided key.

```js
test('passes when object contains the given key', () => {
  const o = { a: 'foo', b: 'bar', c: 'baz' };
  expect(o).toContainKey('a');
  expect(o).toContainKey('b');
  expect(o).toContainKey('c');
  expect(o).not.toContainKey('d');
});
```

### .toContainKeys([keys])

_Note: Currently unimplemented_

Use `.toContainKeys` when checking if an object has all of the provided keys.

```js
test('passes when object contains all keys', () => {
  const o = { a: 'foo', b: 'bar', c: 'baz' };
  expect(o).toContainKeys(['a', 'b']);
  expect(o).toContainKeys(['b', 'c']);
  expect(o).not.toContainKeys(['d']);
});
```

### .toContainAllKeys([keys])

_Note: Currently unimplemented_

Use `.toContainAllKeys` when checking if an object only contains all of the provided keys.

```js
test('passes when object only contains all keys', () => {
  const o = { a: 'hello', b: 'world' };
  expect(o).toContainAllKeys(['a', 'b']);
  expect(o).toContainAllKeys(['b', 'a']);
  expect(o).not.toContainAllKeys(['b']);
});
```

### .toContainAnyKeys([keys])

_Note: Currently unimplemented_

Use `.toContainAnyKeys` when checking if an object contains at least one of the provided keys.

```js
test('passes when object contains at least one matching key', () => {
  const o = { a: 'hello', b: 'world' };
  expect(o).toContainAnyKeys(['a']);
  expect(o).toContainAnyKeys(['b']);
  expect(o).toContainAnyKeys(['b', 'c']);
  expect(o).not.toContainAnyKeys(['c']);
});
```

### .toContainValue(value)

Use `.toContainValue` when checking if an object contains the provided value.

```js
test('passes when object contains given value', () => {
  const o = { a: 'foo', b: 'bar', c: 'baz' };
  expect(o).toContainValue('foo');
  expect(o).toContainValue('bar');
  expect(o).not.toContainValue('qux');
});
```

### .toContainValues([values])

Use `.toContainValues` when checking if an object contains all of the provided values.

```js
test('passes when object contains all of the given values', () => {
  const o = { a: 'foo', b: 'bar', c: 'baz' };
  expect(o).toContainValues(['foo']);
  expect(o).toContainValues(['baz', 'bar']);
  expect(o).not.toContainValues(['qux', 'foo']);
});
```

### .toContainAllValues([values])

_Note: Currently unimplemented_

Use `.toContainAllValues` when checking if an object only contains all of the provided values.

```js
test('passes when object only contains all of the given values', () => {
  const o = { a: 'foo', b: 'bar', c: 'baz' };
  expect(o).toContainAllValues(['foo', 'bar', 'baz']);
  expect(o).toContainAllValues(['baz', 'bar', 'foo']);
  expect(o).not.toContainAllValues(['bar', 'foo']);
});
```

### .toContainAnyValues([values])

_Note: Currently unimplemented_

Use `.toContainAnyValues` when checking if an object contains at least one of the provided values.

```js
test('passes when object contains at least one of the given values', () => {
  const o = { a: 'foo', b: 'bar', c: 'baz' };
  expect(o).toContainAnyValues(['qux', 'foo']);
  expect(o).toContainAnyValues(['qux', 'bar']);
  expect(o).toContainAnyValues(['qux', 'baz']);
  expect(o).not.toContainAnyValues(['qux']);
});
```

### .toContainEntry([key, value])

_Note: Currently unimplemented_

Use `.toContainEntry` when checking if an object contains the provided entry.

```js
test('passes when object contains given entry', () => {
  const o = { a: 'foo', b: 'bar', c: 'baz' };
  expect(o).toContainEntry(['a', 'foo']);
  expect(o).toContainEntry(['b', 'bar']);
  expect(o).toContainEntry(['c', 'baz']);
  expect(o).not.toContainEntry(['a', 'qux']);
});
```

### .toContainEntries([[key, value]])

_Note: Currently unimplemented_

Use `.toContainEntries` when checking if an object contains all of the provided entries.

```js
test('passes when object contains all of the given entries', () => {
  const o = { a: 'foo', b: 'bar', c: 'baz' };
  expect(o).toContainEntries([['a', 'foo']]);
  expect(o).toContainEntries([['c', 'baz'], ['a', 'foo']]);
  expect(o).not.toContainEntries([['b', 'qux'], ['a', 'foo']]);
});
```

### .toContainAllEntries([[key, value]])

_Note: Currently unimplemented_

Use `.toContainAllEntries` when checking if an object only contains all of the provided entries.

```js
test('passes when object only contains all of the given entries', () => {
  const o = { a: 'foo', b: 'bar', c: 'baz' };
  expect(o).toContainAllEntries([['a', 'foo'], ['b', 'bar'], ['c', 'baz']]);
  expect(o).not.toContainAllEntries([['a', 'foo'], ['b', 'bar']]);
});
```

### .toContainAnyEntries([[key, value]])

_Note: Currently unimplemented_

Use `.toContainAnyEntries` when checking if an object contains at least one of the provided entries.

```js
test('passes when object contains at least one of the given entries', () => {
  const o = { a: 'foo', b: 'bar', c: 'baz' };
  expect(o).toContainAnyEntries([['a', 'qux'], ['a', 'foo']]);
  expect(o).toContainAnyEntries([['a', 'qux'], ['b', 'bar']]);
  expect(o).toContainAnyEntries([['a', 'qux'], ['c', 'baz']]);
  expect(o).not.toContainAnyEntries([['d', 'qux']]);
});
```

### .toSatisfy(predicate)

_Note: Currently unimplemented_

Use `.toSatisfy` when you want to use a custom matcher by supplying a predicate function that returns a `Boolean`.

```js
test('passes when value passes given predicate', () => {
  const greaterThanOneButNotThree = n => n > 1 && n !== 3;
  expect(100).toSatisfy(greaterThanOneButNotThree);
  expect(0).not.toSatisfy(greaterThanOneButNotThree);
  expect(3).not.toSatisfy(greaterThanOneButNotThree);
});
```

### .toHaveAllMembers([members])

_Note: Currently unimplemented_

Use `.toHaveAllMembers` when checking if an `Array` contains all of the same members of a given set.

```js
test('passes when given array values match the members of the set', () => {
  expect([1, 2, 3]).toHaveAllMembers([2, 1, 3]);
  expect([1, 2, 2]).toHaveAllMembers([2, 1]);
});
```

### .toHaveSomeMembers([members])

_Note: Currently unimplemented_

Use `.toHaveSomeMembers` when checking if an `Array` contains some of the members of a given set.

```js
test('passes when given array values match the members of the set', () => {
  expect([1, 2, 3]).toHaveSomeMembers([2, 1, 3]);
  expect([1, 2, 2]).toHaveSomeMembers([2]);
  expect([1, 2, 2]).not.toHaveSomeMembers([3]);
});
```

### .toBeOneOf([members])

Use `.toBeOneOf` when checking if a value is a member of a given `Array`.

```js
test('passes when value is in given array', () => {
  expect(1).toBeOneOf([1, 2, 3]);
  expect(4).not.toBeOneOf([1, 2, 3]);
});
```

### .toBeExtensible()

Use `.toBeExtensible` when checking if an object is extensible.

```js
test('passes when value is extensible', () => {
  expect({a: 1}).toBeExtensible();
  expect(1).not.toBeExtensible();
});
```

### .toBeSealed()

_Note: Currently unimplemented_

Use `.toBeSealed` when checking if an object is sealed.

```js
test('passes when value is sealed', () => {
  expect(Object.seal({})).toBeSealed();
  expect({}).not.toBeSealed();
  expect(1).not.toBeSealed();
});
```

### .toBeFrozen()

Use `.toBeFrozen` when checking if an object is frozon.

```js
test('passes when value is frozen', () => {
  expect(Object.frozen({})).toBeFrozen();
  expect({}).not.toBeFrozen();
  expect(1).not.toBeFrozen();
});
```

### .toBeFinite()

_Note: Currently unimplemented_

Use `.toBeFinite` when checking if a value is a `Number`, not `NaN` or `Infinity`.

```js
test('passes when value is a finite number', () => {
  expect(1).toBeFinite();
  expect(Infinity).not.toBeFinite();
  expect(NaN).not.toBeFinite();
});
```

### .toBePositive()

_Note: Currently unimplemented_

Use `.toBePositive` when checking if a value is a positive `Number`.

```js
test('passes when value is a positive number', () => {
  expect(1).toBePositive();
  expect(Infinity).not.toBePositive();
  expect(-1).not.toBePositive();
  expect(NaN).not.toBePositive();
});
```

### .toBeNegative()

Use `.toBeNegative` when checking if a value is a negative `Number`.

```js
test('passes when value is a negative number', () => {
  expect(-1).toBeNegative();
  expect(-Infinity).not.toBeNegative();
  expect(1).not.toBeNegative();
  expect(NaN).not.toBeNegative();
});
```

### .toBeEven()

_Note: Currently unimplemented_

Use `.toBeEven` when checking if a value is an even `Number`.

```js
test('passes when value is an even number', () => {
  expect(2).toBeEven();
  expect(1).not.toBeEven();
  expect(NaN).not.toBeEven();
});
```

### .toBeOdd()

_Note: Currently unimplemented_

Use `.toBeOdd` when checking if a value is an odd `Number`.

```js
test('passes when value is an odd number', () => {
  expect(1).toBeOdd();
  expect(2).not.toBeOdd();
  expect(NaN).not.toBeOdd();
});
```

### .toBeFunction()

_Note: Currently unimplemented_

Use `.toBeFunction` when checking if a value is a `Function`.

```js
test('passes when value is a function', () => {
  function noop = () {};
  expect(() => {}).toBeFunction();
  expect(function() {}).not.toBeFunction();
  expect(noop).toBeFunction();
  expect(true).not.toBeFunction();
});
```

### .toBeObject()

_Note: Currently unimplemented_

Use `.toBeObject` when checking if a value is an `Object`.

```js
test('passes when value is an object', () => {
  expect({}).toBeObject();
  expect({ a: 'hello' }).toBeObject();
  expect(true).not.toBeObject();
});
```

### .toBeArray()

_Note: Currently unimplemented_

Use `.toBeArray` when checking if a value is an `Array`.

```js
test('passes when value is an array', () => {
  expect([]).toBeArray();
  expect([1]).toBeArray();
  expect(true).not.toBeArray();
});
```

### .toBeString()

Use `.toBeString` when checking if a value is a `String`.

```js
test('passes when value is a string', () => {
  expect('').toBeString();
  expect('hello').toBeString();
  expect(new String('hello')).toBeString();
  expect(true).not.toBeString();
});
```

### .toBeNumber()

_Note: Currently unimplemented_

Use `.toBeNumber` when checking if a value is a `Number`.

```js
test('passes when value is a number', () => {
  expect(1).toBeNumber();
  expect(NaN).toBeNumber();
  expect(Infinity).toBeNumber();
  expect(true).not.toBeNumber();
});
```

### .toBeBoolean()

_Note: Currently unimplemented_

Use `.toBeBoolean` when checking if a value is a `Boolean`.

```js
test('passes when value is a boolean', () => {
  expect(false).toBeBoolean();
  expect(true).toBeBoolean();
  expect(1 === 1).toBeBoolean();
  expect(1).not.toBeBoolean();
});
```

### .toStartWith(prefix)

Use `.toStartWith` when checking if a `String` starts with a given `String` prefix.

```js
test('passes when value is starts with given string', () => {
  expect('hello world').toStartWith('hello');
  expect('hello world').not.toStartWith('world');
});
```

### .toEndWith(suffix)

Use `.toEndWith` when checking if a `String` ends with a given `String` suffix.

```js
test('passes when value is ends with given string', () => {
  expect('hello world').toEndWith('world');
  expect('hello world').not.toEndWith('hello');
});
```

### .toInclude(substring)

_Note: Currently unimplemented_

Use `.toInclude` when checking if a `String` includes the given `String` substring.

```js
test('passes when value includes substring', () => {
  expect('hello world').toInclude('ell');
  expect('hello world').not.toInclude('bob');
});
```

### .toIncludeRepeated(substring, times)

_Note: Currently unimplemented_

Use `.toIncludeRepeated` when checking if a `String` includes the given `String` substring the correct number of times.

```js
test('passes when value includes substring n times', () => {
  expect('hello hello world').toIncludeRepeated('hello', 2);
  expect('hello hello world').not.toIncludeRepeated('hello', 1);
});
```

### .toIncludeMultiple([substring])

Use `.toIncludeMultiple` when checking if a `String` includes all of the given substrings.

```js
test('passes when value includes all substrings', () => {
  expect('hello world').toInclude(['world', 'hello']);
  expect('hello world').not.toInclude(['world', 'hello', 'bob']);
});
```

### .toEqualCaseInsensitive(string)

Use `.toEqualCaseInsensitive` when checking if a string is equal (===) to another ignoring the casing of both strings.

```js
test('passes when strings are equal ignoring case', () => {
  expect('hello world').toEqualCaseInsensitive('hello world');
  expect('hello WORLD').toEqualCaseInsensitive('HELLO world');
  expect('HELLO WORLD').toEqualCaseInsensitive('hello world');
  expect('hello world').toEqualCaseInsensitive('HELLO WORLD');
  expect('hello world').not.toEqualCaseInsensitive('hello');
});
```

## Contributors

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
| [<img src="https://avatars0.githubusercontent.com/u/5610087?v=4" width="100px;"/><br /><sub>Matt Phillips</sub>](http://mattphillips.io)<br />[📝](#blog-mattphillips "Blogposts") [💻](https://github.com/mattphillips/jest-extended/commits?author=mattphillips "Code") [📖](https://github.com/mattphillips/jest-extended/commits?author=mattphillips "Documentation") [💡](#example-mattphillips "Examples") [🚇](#infra-mattphillips "Infrastructure (Hosting, Build-Tools, etc)") [⚠️](https://github.com/mattphillips/jest-extended/commits?author=mattphillips "Tests") | [<img src="https://avatars1.githubusercontent.com/u/20847518?v=4" width="100px;"/><br /><sub>Brandon Newton</sub>](https://btnwtn.com)<br />[💻](https://github.com/mattphillips/jest-extended/commits?author=btnwtn "Code") [📖](https://github.com/mattphillips/jest-extended/commits?author=btnwtn "Documentation") [⚠️](https://github.com/mattphillips/jest-extended/commits?author=btnwtn "Tests") | [<img src="https://avatars2.githubusercontent.com/u/8472688?v=4" width="100px;"/><br /><sub>Gary Leutheuser</sub>](https://GaryLeutheuser.github.io)<br />[💻](https://github.com/mattphillips/jest-extended/commits?author=GaryLeutheuser "Code") | [<img src="https://avatars3.githubusercontent.com/u/24882614?v=4" width="100px;"/><br /><sub>Johan Lindgren</sub>](https://github.com/lindgr3n)<br />[💻](https://github.com/mattphillips/jest-extended/commits?author=lindgr3n "Code") [📖](https://github.com/mattphillips/jest-extended/commits?author=lindgr3n "Documentation") [⚠️](https://github.com/mattphillips/jest-extended/commits?author=lindgr3n "Tests") | [<img src="https://avatars1.githubusercontent.com/u/159848?v=4" width="100px;"/><br /><sub>Andrew Hayward</sub>](http://andrewhayward.net)<br />[💻](https://github.com/mattphillips/jest-extended/commits?author=andrewhayward "Code") [⚠️](https://github.com/mattphillips/jest-extended/commits?author=andrewhayward "Tests") | [<img src="https://avatars3.githubusercontent.com/u/6209178?v=4" width="100px;"/><br /><sub>Oliver Schneider</sub>](https://ols.io)<br />[💻](https://github.com/mattphillips/jest-extended/commits?author=olsio "Code") [⚠️](https://github.com/mattphillips/jest-extended/commits?author=olsio "Tests") | [<img src="https://avatars1.githubusercontent.com/u/22359375?s=460&v=4" width="100px;"/><br /><sub>Tyle Whalen</sub>](https://github.com/tjwhalen16)<br />[💻](https://github.com/mattphillips/jest-extended/commits?author=tjwhalen16 "Code") [📖](https://github.com/mattphillips/jest-extended/commits?author=tjwhalen16 "Documentation") |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| [<img src="https://avatars2.githubusercontent.com/u/17944339?v=4" width="100px;"/><br /><sub>Martius</sub>](https://github.com/martiuslim)<br />[💻](https://github.com/mattphillips/jest-extended/commits?author=martiuslim "Code") [⚠️](https://github.com/mattphillips/jest-extended/commits?author=martiuslim "Tests") | [<img src="https://avatars2.githubusercontent.com/u/10856932?v=4" width="100px;"/><br /><sub>Eli Collis</sub>](https://github.com/ecollis6)<br />[💻](https://github.com/mattphillips/jest-extended/commits?author=ecollis6 "Code") | [<img src="https://avatars0.githubusercontent.com/u/10706203?v=4" width="100px;"/><br /><sub>Marcin Lichwała</sub>](https://github.com/marcinlichwala)<br />[💻](https://github.com/mattphillips/jest-extended/commits?author=marcinlichwala "Code") [⚠️](https://github.com/mattphillips/jest-extended/commits?author=marcinlichwala "Tests") | [<img src="https://avatars3.githubusercontent.com/u/1984733?v=4" width="100px;"/><br /><sub>Massimo Prencipe</sub>](https://github.com/mprencipe)<br />[💻](https://github.com/mattphillips/jest-extended/commits?author=mprencipe "Code") [⚠️](https://github.com/mattphillips/jest-extended/commits?author=mprencipe "Tests") |
<!-- ALL-CONTRIBUTORS-LIST:END -->

## LICENSE

MIT
