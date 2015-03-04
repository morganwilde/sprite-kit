# SKNode

All visual elements in a SpriteKit game are drawn using predefined `SKNode` subclasses.

List of subclasses:

1. `SKSpriteNode` - draws a textured sprite
1. `SKVideoNode` - plays a video
1. [`SKLabelNode`](https://github.com/morganwilde/sprite-kit/blob/master/sk-morganwilde-SKLabelNode.md) - renders a string
1. `SKShapeNode` - renders a shape
1. `SKEmitterNode` - creates and renders particles
1. `SKCropNode` - crops
1. `SKEffectNode` - applies a Core Image filter to children
1. `SKLightNode` - lighting and shadows for a scene
1. `SKFieldNode` - applies physics effects to a portion of a scene

Nodes are organised into a tree structure. `SKNode` does not draw anything itself, but subclasses do. Every node provides a coordinate system to its children. It also has a `frame` and `calculateAccumulatedFrame` to determine the size.

Nodes can respond to user actions. Nodes can support a physics body and have constraints that express relationships with other nodes in the scene.

Their primary usage is to organised other nodes, specifically subclasses of `SKNode` into groups.

Nodes have names and they are used to identify them. Searches can be done using names, using `childNodeWithName:` and similar methods.

SKNode can be subclasses, but not for drawing.

# Methods and examples

```Swift
init() // Empty node
convenience init!(fileNamed filename: String) // Used to load nodes from archive in the game bundle
var frame: CGRect // Frame within parent, ignoring children
func calculateAccumulatedFrame() -> CGRect // Frame including children
var position: CGPoint // Position within parent
var zPosition: CGFloat // Used to bring node forward/backward
func setScale(_ scale: CGFloat) // Scales x and y
var zRotation: CGFloat // Counterclockwise rotation
var alpha: CGFloat // Visibility factor
var hidden: Bool // Is this node shown
var userInteractionEnabled: Bool // Same as with views
func addChild(_ node: SKNode) // Main way to create node tree
func removeFromParent() // Removes this node from parent
var children: [AnyObject] // Children nodes
var parent: SKNode? // Parent node
var scene: SKScene? // Scene node
var name: String? // Node name
func runAction(_ action: SKAction!) // Executes an action for the next animation loop
func runAction(_ action: SKAction!, completion block: (() -> Void)!) // With a completion block
var physicsBody: SKPhysicsBody? // If the node participates in physics simulation
var constraints: [AnyObject]? // The sum total of all constraints applied to this node
```
