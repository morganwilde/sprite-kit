#SKScene

`SKScene` is used to represent a scene of content in `SpriteKit`. It is the root node in a tree of `SpriteKit` nodes (`SKNode`).

Scene calculates the cotents of a new frame by processing these actions:

1. update
2. Executes options on its children
3. didEvaluateActions
4. Executes physics simulations on physics bodies inside the scene
5. didSimulatePhysics
6. Applies constraints on nodes inside the scene
7. didApplyConstraints
8. didFinishUpdate
9. Renders all the nodes and updates the view to display the new contents

##Methods

- init 

Creates a scene with an optional size given

```Swift
    let skScene = SKScene()
    let skSizedScene = SKScene(size: CGSize(width: 100, height: 100))
```

- update

Performs any scene-specific updates that need to occur before scene actions are evaluated.

- didEvaluateActions
- didSimulatePhysics
- didApplyConstraints
- didFinishUpdate

##Properties

- backgroundColor : NSColor
    skScene.backgroundColor = UIColor.blackColor()