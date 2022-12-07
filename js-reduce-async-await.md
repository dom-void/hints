```js
let arr = [1, 2, 3, 4, 5, 6, 7, 8, 9]

const getTimeStamp = () => {
    return new Promise((res, rej) => {
        return setTimeout(() => {
            res(new Date().getTime())
        }, 300)
    })
}

/**
* for … of …
*/

let result = [];

for (let el of arr) {
    result.push(await getTimeStamp())
}

console.log(result)
// [1670401774882, 1670401775195, 1670401775508, 1670401775820, 1670401776134, 1670401776446, 1670401776757, 1670401777071, 1670401777387]

/**
* reduce
*/

await arr.reduce(async (acc, el) => {
    const timeStamp = await getTimeStamp();
    return [...(await acc), el + timeStamp];
}, [])
// [1670401904432, 1670401904433, 1670401904434, 1670401904435, 1670401904436, 1670401904437, 1670401904438, 1670401904439, 1670401904440]
```

[How to use async functions with Array.reduce in Javascript](https://advancedweb.hu/how-to-use-async-functions-with-array-reduce-in-javascript/)
