## Task:
Write a function that takes a single string (`word`) as argument. The function must return an ordered list containing the indexes of all capital letters in the string.

**Example**
```javascript
Test.assertSimilar( capitals('CodEWaRs'), [0,3,4,6] );
```

<br />

### Solution:
```javascript
var capitals = function (word) {
  return [...word].map((item, index) => item===item.toUpperCase() ? index : null).filter(i => i !== null)
};
```