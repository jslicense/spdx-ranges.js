```shellsession
$ npm install spdx-ranges
```

```javascript
var assert = require('assert')
var spdxRanges = require('spdx-ranges')

assert(
  Array.isArray(spdxRanges),
  'module is an Array')

assert(
  spdxRanges.length > 0,
  'the Array has elements')

assert(
  spdxRanges.every(function(e) {
    return Array.isArray(e) }),
  'each Array element is an Array')

assert(
  spdxRanges.every(function(range) {
    return range.every(function(identifier) {
	  return typeof identifier === 'string' }) }),
  'elements of Array-elements are strings')
```
