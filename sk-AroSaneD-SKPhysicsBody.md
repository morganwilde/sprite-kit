#SKPhysicsBody
An **SKPhysicsBody** object is used to add physics simulation to a node.

Sprite Kit supports two kinds of physics bodies, **volume-based bodies** and **edge-based bodies**.

**volume-based bodies** have a mass and volume, so they are affected by all physics simulations if the **_dynamic_** property is set to true. <br /> 
**edge-based bodies** do not have mass or volume. They are somewhat like static objects (volume-less boundaries, hollow spaces, etc).

1. init(...). There are multiple examples of the init(...) methods, all of which are used to create the physics body. They all accept different parameters, ranging from circles, to recatngles, to coordinates, to paths, to textures, to existing bodies. <br /> 
```Swift
init(circleOfRadius r: CGFloat,
	center center: CGPoint) -> SKPhysicsBody
```

2. creatingEdges. There a few methods to create edges as well.
```Swift
init(edgeFromPoint p1: CGPoint,
	toPoint p2: CGPoint) -> SKPhysicsBody
```

Properties: <br />

1. affectedByGravity: Bool
1. allowsRotation: Bool
1. dynamic: Bool
1. mass: CGFloat
1. density: CGFloat
1. area: CGFloat { get }
1. friction: CGFloat
1. restitution: CGFloat
1. linearDamping: CGFloat
1. angularDamping: CGFloat
1. categoryBitMask: UInt32 - used to control whith whom bodies interact (base)
1. collisionBitMask: UInt32 - tell which categories can collide with it
and so on