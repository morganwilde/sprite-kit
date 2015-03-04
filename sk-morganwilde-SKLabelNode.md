# SKLabelNode

`SKLabelNode` draws text. Since SpriteKit is implemented using OpenGL and there is no native text handling features in OpenGL, it would extremely difficult to implement text drawing on your own. This class takes care of that.

The size of this node is implicitly determined by the font, font size and text properties.

# Methods and code examples

```Swift
let labelNode = SKLabelNode(fontNamed: "Helvetica")
labelNode.text = "Example"
labelNode.fontSize = 30
labelNode.fontColor = UIColor.blackColor()
labelNode.position = CGPoint(
    x: 0,
    y: 0)
```

### Methods and properties

```Swift
init(fontNamed fontName: String!) // The designated initialiser
var text: String // Container for the text
var fontColor: UIColor // Color for the entire label
var fontSize: CGFloat // Size in points (32 default)
// Alignment
// Possible values:
// - .Baseline
// - .Center
// - .Top
// - .Bottom
var verticalAlignmentMode: SKLabelVerticalAlignmentMode
// Possible values:
// - .Center
// - .Left
// - .Right
var horizontalALignmentMode: SKLabelHorizontalAlignmentMode
```
