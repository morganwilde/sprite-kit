# SKCropNode

Takes one node as a mask and applies that mask to all of the children nodes of the `SKCropNode` instance.

# Methods and code examples

```Swift
var maskNode: SKNode? // The node that will mask other nodes; do not add this to the hierarchy
```

The `maskNode` is the first one to be rendered and used to crop children nodes.

```Swift
let cropNode = SKCropNode()

let nodeBackground = SKNode() // A single child node to be masked
let nodeMask = SKNode() // The node that will mask all children nodes

cropNode.maskNode = nodeMask
cropNode.addChild(nodeBackground)
```
