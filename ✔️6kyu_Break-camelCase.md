## Task:
Complete the solution so that the function will break up camel casing, using a space between words.
<br />  
**Example**

```
"camelCasing"  =>  "camel Casing"
"identifier"   =>  "identifier"
""             =>  ""
```
<br />  

### Solution:

```javascript
function solution(string) {
  return string.replace(/[A-Z]/g, " $&");
}
```