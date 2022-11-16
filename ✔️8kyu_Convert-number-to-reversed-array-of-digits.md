## Task:
Given a random non-negative number, you have to return the digits of this number within an array in reverse order.

<br />

**Example(Input => Output)**:

```
35231 => [1,3,2,5,3]
0 => [0]
```

<br />

### Solution:
```javascript
function digitize(n) {
  return (Array.from(String(n), Number)).reverse()
}
```