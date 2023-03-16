# `XML` parsing example

```js
let fetchXML = (url) => {
    const res = await fetch(url);
    const data = await res.text();
    const parsed = new DOMParser().parseFromString(text,"text/xml");
    return parsed;
}
```
