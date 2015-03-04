#SKView

Used to display `SpriteKit` content. The content is provided by an `SKScene` object.

To add a scene to the `SKView`, you need to 

#Methods

- presentScene(_scene: SKScene?, transition: SKTransition?)

>> Adds a scene to the view while also removing the old ones. Can provide a transition object.

    let skView = SKView()
    let skScene = SKScene()
    let transition = SKTransition()

    // Add the scene to the view
    skView.presentScene(skScene)

    // With a transition
    skView.presentScene(skScene, transition: transition)


#Propety

- asynchronous : Bool
    
>> If true the scene will be rendered asynchronously









1. First ordered list item
2. Another item
⋅⋅* Unordered sub-list. 
1. Actual numbers don't matter, just that it's a number
⋅⋅1. Ordered sub-list
4. And another item.
