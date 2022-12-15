## DESCRIPTION:

Some numbers have funny properties. For example:

> <i>"89 --> 8<sup>1</sup> + 9<sup>2</sup> = 89 * 1"</i>

> <i>"695 --> 6<sup>2</sup> + 9<sup>3</sup> + 5<sup>4</sup> = 1390 = 695 * 2"</i>

> <i>"46288 --> 4<sup>3</sup> + 6<sup>4</sup> + 2<sup>5</sup> + 8<sup>6</sup> + 8<sup>7</sup> = 2360688 = 46288 * 51"</i>

Given a positive integer n written as abcd... (a, b, c, d... being digits) and a positive integer p

* we want to find a positive integer k, if it exitsts, such that hte sum of the digits of n taken to the successive powers of p is equal to k * n.

In other words:

> <i>"Is there an integer k such as: (a<sup>p</sup> + b<sup>p+1</sup> + c<sup>p+2</sup> + d<sup>p+3</sup> + ...) = n * k"</i>

If it is the case we will return k, if not return -1.

**Note:** n and p will alwaysbe given as strictly positive integers.

```js
digPow(89, 1) should return 1 since 8^1 + 9^2 = 89 = 89 * 1

digPow(92, 1) should return -1 since there is no k such as 9^1 + 2^2 equals 92 * k

digPow(695, 2) should return 2 since 6^2 + 9^3 + 5^4 = 1390 = 695 * 2

digPow(46288, 3) should return 51 since 4^3 + 6^4 + 2^5 + 8^6 + 8^7 = 2360688 = 46288 * 51
```

<br />

### Solution:
```js
function digPow(n, p) {
    const result = n.toString().split("").map((i, id) => i**(id+p)).reduce((sum, num) => sum + num, 0)
    return (result % n === 0) ? result/n : -1
}
```