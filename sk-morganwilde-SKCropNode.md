# SKCropNode

Takes one node as a mask

# Methods and code examples

The `maskNode` is the first one to be rendered and used to crop children nodes.

```Swift
let cropNode = SKCropNode()

let nodeBackground = SKNode() // A single child node to be masked
let nodeMask = SKNode() // The node that will mask all children nodes

cropNode.maskNode = nodeMask
cropNode.addChild(nodeBackground)
```
