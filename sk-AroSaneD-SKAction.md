# SKAction


## Summary

An SKAction object is an action that is executed by a node in the scene (SKScene). Actions are most often used to change the structure and content of the node to which they are attached but can also make other changes to the scene. 

Most actions allow you to change a node’s properties, such as its position, rotation, or scale. 

Many actions can be reversed, allowing you to create another action object that reverses the effect of that action. (By calling the _reversedAction_ method)

Some actions include other actions as children:
1. Sequence action
2. Group action
3. Repeating action

These actions can be nested, in order to obtain highly sophisticated behaviour for nodes.


__Main methods:__

1. __moveByX__

```Swift
class func moveByX(
	_ deltaX: CGFloat,
	y deltaY: CGFloat,
	duration sec: NSTimeInterval) -> SKAction
```

This does what it says. 
deltaX and deltaY - the points to add to the nodes position. 
sec - the duration of the action (in seconds).

There are many others like this (moveByX, moveByDuration, moveTo etc.)	<br />	    
2. __followPath__<br />

		    class func followPath(_ path: CGPath,
             duration sec: NSTimeInterval) -> SKAction
Sets the node to follow a certain (fixed) path.


path - A Core Graphics path whose coordinates are relative to the node’s current position.
sec	 - The duration of the animation.

Similar methods also exists, but accept different parameters, work in different ways. <br /> <br />
3. __speedBy__

		    class func speedTo(_ speed: CGFloat,
          duration sec: NSTimeInterval) -> SKAction
Increases the speed at which a node performs its action.

speed - The new value for the node’s speed.<br />
sec	 - The duration of the animation.

This action is not reversible, and doen't have any methods with similar behavior.

### And generally, anything that you can think of - there's probably an action for it. If not, devide it into subaction and search for them.
<br />
## Example!

		func fireProjectile() {
        let projectile = self.dynamicType.projectile.copy() as SKSpriteNode
        projectile.position = position
        projectile.zRotation = zRotation
        
        let waitAction = SKAction.waitForDuration(Constants.projectileFadeOutDuration)
        let fadeAction = SKAction.fadeOutWithDuration(Constants.projectileLifetime - Constants.projectileFadeOutDuration)
        let removeAction = SKAction.removeFromParent()
        let sequence = [waitAction, fadeAction, removeAction]
 
        projectile.runAction(SKAction.sequence(sequence))      
    }
	
__Very general example, but all actions follow this format.__
	    