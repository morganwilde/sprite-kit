#SKView

Used to display `SpriteKit` content. The content is provided by an `SKScene` object.

#Methods

- presentScene(_scene: SKScene?, transition: SKTransition?)

Adds a scene to the view while also removing the old ones. Can provide a transition object.

    let skView = SKView()
    let skScene = SKScene()
    let transition = SKTransition()

    // Add the scene to the view
    skView.presentScene(skScene)

    // With a transition
    skView.presentScene(skScene, transition: transition)

- convertPoint

Converts a point from coordinates to view coordinates

    let skView = SKView()
    let skScene = SKScene()

    let point = CGPoint(x: 5, y: 10)
    let pointInView = skView.convertPoint(point, fromScene: skScene)

#Propety

- asynchronous : Bool
    
If true the scene will be rendered asynchronously

- paused : Bool

If true, fixes the scenes content onscreen. No actions are executed and no physics simulation is performed.


###Debugging properties

- showsFPS : Bool
- showsQuadCount : Bool
Displays the number of rectangles used to render the scene
- showsDrawCount : Bool
Displays the number of drawing passed needed to render the view
- showsNodeCount : Bool
- showsPhysics : Bool
Each time a frame is rendered, an image is drawn behind your scene that shows the effects of any physics fields contained in the scene.