#SKTransition

`SKTransition` is used to perform an animated transition between the current and incoming `SKScene`s in an `SKView` object.

##Static Methods

- doorsOpenHorizontalWithDuration

```Swift
let doorsOpenX = SKTransition.doorsOpenHorizontalWithDuration(2.0)
kView.presentScene(skScene, transition: doorsOpenX)
```

- revealWithDirection(direction: SKTransitionDirection, duration: NSTimeInterval)

Creates a transition where the old scene moves out of the view, revealing the new scene underneath it.

```Swift
let reveal = SKTransition.revealWithDirection(SKTransitionDirection.Right, duration: 15.0)
```




##Properties

- pausesOutgoingScene : Bool

If true, the outgoing scene will be paused during the transition. Default value = true