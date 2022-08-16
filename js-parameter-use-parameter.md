# Default parameter value takes other parameter declared before

```js
function test(x, y, z = x + y) {
  console.log(z);
};

test(1, 1, 1); // 1
test(1, 2); // 3
```
