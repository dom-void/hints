# Destructuring assignment example

```js
const product = {
  id: 0,
  name: "computer",
  imageUrls: [
    "front.jpg",
    "side.jpg",
    "back.jpg"
  ],
  extentions: {
    ports: [
      "usb2",
      "usb3",
      "lan"
    ],
  },
  included: [
    "monitor",
    "wires",
    "mouse",
  ],
};

const {
  imageUrls: images, // destructure `imageUrls` as `images
  extentions: {
    ports: connections, // destructure `ports` as `connections`
  },
  included: additional, // destructure `included` as `additional`
  additionalEq = [ // added new property with default value
    ...additional, // spreaded value
    "cover",
    "keyboard",
  ],
} = product;

console.log(images, connections, additionalEq);
// (3) ["front.jpg", "side.jpg", "back.jpg"], (3) ["usb2", "usb3", "lan"], (5) ["monitor", "wires", "mouse", "cover", "keyboard"]
```
