## Task:
Given a string of words, you need to find the highest scoring word.

Each letter of a word scores points according to its position in the alphabet: `a = 1, b = 2, c = 3` etc.

You need to return the highest scoring word as a string.

If two words score the same, return the word that appears earliest in the original string.

All letters will be lowercase and all inputs will be valid.

<br />

### Solution:
```javascript
function highest(x) {
    const arr = x.split(" ");
    const charCodeArr = arr.map(word => [...word].reduce((sum, i) => sum + (i.charCodeAt(0) - 96), 0))
    return arr[charCodeAt.indexOf(Math.max(...charCodeArr))]
}
```