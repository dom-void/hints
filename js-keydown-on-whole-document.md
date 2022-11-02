# A `keydown` on whole `HTML` document

```js
document.onkeydown = function(evt) {
    evt = evt || window.event;
    if (evt.keyCode == 32) {
        alert("You hit a space");
    }
};
```

[Capture key press without placing an input element on the page?](https://stackoverflow.com/questions/2878983/capture-key-press-without-placing-an-input-element-on-the-page)

[JavaScript Madness: Keyboard Events](https://unixpapa.com/js/key.html)
