## Task:
The rgb function is incomplete. Complete it so that passing in RGB decimal values will result in a hexadecimal representation being returned. Valid decimal values for RGB are 0 - 255. Any values that fall out of that range must be rounded to the closest valid value.

Note: Your answer should always be 6 characters long, the shorthand with 3 will not work here.

The following are examples of expected output values:
```javascript
rgb(255, 255, 255) // returns FFFFFF
rgb(255, 255, 300) // returns FFFFFF
rgb(0,0,0) // returns 000000
rgb(148, 0, 211) // returns 9400D3
```

<br />

### Solution:
```javascript
function rgb(r, g, b){
  const compToHex = (c) => {
    const hex = (c > 255 ? 255 : c < 0 ? 0 : c).toString(16)
    return hex.length === 1 ? "0" + hex : hex
  }
  return (compToHex(r) + compToHex(g) + compToHex(b)).toUpperCase()
}
```