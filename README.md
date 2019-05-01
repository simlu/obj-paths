# obj-paths

[![Build Status](https://circleci.com/gh/blackflux/obj-paths.png?style=shield)](https://circleci.com/gh/blackflux/obj-paths)
[![Test Coverage](https://img.shields.io/coveralls/blackflux/obj-paths/master.svg)](https://coveralls.io/github/blackflux/obj-paths?branch=master)
[![Dependabot Status](https://api.dependabot.com/badges/status?host=github&repo=blackflux/obj-paths)](https://dependabot.com)
[![Dependencies](https://david-dm.org/blackflux/obj-paths/status.svg)](https://david-dm.org/blackflux/obj-paths)
[![NPM](https://img.shields.io/npm/v/obj-paths.svg)](https://www.npmjs.com/package/obj-paths)
[![Downloads](https://img.shields.io/npm/dt/obj-paths.svg)](https://www.npmjs.com/package/obj-paths)
[![Semantic-Release](https://github.com/blackflux/js-gardener/blob/master/assets/icons/semver.svg)](https://github.com/semantic-release/semantic-release)
[![Gardener](https://github.com/blackflux/js-gardener/blob/master/assets/badge.svg)](https://github.com/blackflux/js-gardener)

Utility functions around object paths

## Install

    $ npm i --save obj-paths

## Usage

<!-- eslint-disable import/no-unresolved, import/no-extraneous-dependencies -->
```js
const objectPaths = require('obj-paths');

objectPaths.split('data(file1,file2)');
// => ["data.file1", "data.file2"]
objectPaths.join(['data', 'data']);
// => "data"
objectPaths.join(['path.to.thing', 'path.to.other.thing']);
// => "path.to(thing,other.thing)"
objectPaths.getParents(['child', 'parent.child', 'grandparent.parent.child']);
// => ['parent', 'grandparent', 'grandparent.parent']
```

## Methods

### split

Takes a shortened input string and separates it into an array.

### join

Takes array of selectors and shortens it into a string

### getParents

Takes array of selectors and returns unique, true parents.

### retain

Takes object and array of selectors. Removes non selected fields from object.

## Known Limitations

This package does not currently support escaping.
