# yoga-layout-prebuilt [![test](https://github.com/vadimdemedes/yoga-layout-prebuilt/workflows/test/badge.svg)](https://github.com/vadimdemedes/yoga-layout-prebuilt/actions)

> Prebuilt [yoga-layout](https://github.com/facebook/yoga) package

## Usage

```js
import { Yoga } from 'https://code4fukui.github.io/yoga-layout-prebuilt-es/Yoga.js';

const Node = Yoga.Node;

const root = Node.create();
root.setWidth(500);
root.setHeight(300);
root.setJustifyContent(Yoga.JUSTIFY_CENTER);

const node1 = Node.create();
node1.setWidth(100);
node1.setHeight(100);

const node2 = Node.create();
node2.setWidth(100);
node2.setHeight(100);

root.insertChild(node1, 0);
root.insertChild(node2, 1);

root.calculateLayout(500, 300, Yoga.DIRECTION_LTR);

console.log(root.getComputedLayout());
// -> {left: 0, top: 0, width: 500, height: 300}
console.log(node1.getComputedLayout());
// -> {left: 150, top: 0, width: 100, height: 100}
console.log(node2.getComputedLayout());
// -> {left: 250, top: 0, width: 100, height: 100}
```


## License

MIT © [Vadim Demedes](https://github.com/vadimdemedes/yoga-layout-prebuilt)
