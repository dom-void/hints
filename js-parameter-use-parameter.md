# Default parameter value takes other parameter declared before

```js
function test(x, y, z = x + y) {
  console.log(z);
};

test(1, 1, 1); // 1
test(1, 2); // 3
```

> https://www.instagram.com/p/ChTtaCerK9b/?igshid=YmMyMTA2M2Y%3D
