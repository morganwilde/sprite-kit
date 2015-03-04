#SKPhysicsBody
An **SKPhysicsBody** object is used to add physics simulation to a node.

Sprite Kit supports two kinds of physics bodies, **volume-based bodies** and **edge-based bodies**.

**volume-based bodies** have a mass and volume, so they are affected by all physics simulations if the **_dynamic_** property is set to true. <br /> 
**edge-based bodies** do not have mass or volume. They are somewhat like static objects (volume-less boundaries, hollow spaces, etc).

1. init(...). There are multiple examples of the init(...) methods, all of which are used to create the physics body. They all accept different parameters, ranging from circles, to recatngles, to coordinates. <br /> 
```Swift
init(circleOfRadius r: CGFloat,
	center center: CGPoint) -> SKPhysicsBody
```

2.  