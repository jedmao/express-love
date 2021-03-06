# Installation

    npm install @express-love/map-values-async

# Usage

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

## mapValuesAsync

Creates a shallow clone of the specified `source` object. Any properties of
the source object that are promises will be replaced with the resolved value.

### Parameters

-   `source` **[Object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object)** An object with properties that might be promises

### Examples

```javascript
const result = await mapValuesAsync({
  a: Promise.resolve('apples'),
  b: Promise.resolve('bananas'),
  c: 'corn',
});

expect(result).toEqual({
  a: 'apples',
  b: 'bananas',
  c: 'corn',
});
```

Returns **[Object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object)** A clone of `source` with the promise properties replaced with their
