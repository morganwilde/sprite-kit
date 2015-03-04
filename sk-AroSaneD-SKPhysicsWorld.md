# SKPhysicsWorld
An SKPhysicsWorld object simulates collisions and other physical properties. Not to be used by itself, but from reading a scenes **physicsWorld** property.

The physics world object allows you to perform the following tasks:

1. Set global properties for the simulation, such as gravity
1. Create joints between two physics bodies in the scene
1. Set a delegate to receive notifications when two physics bodies are in contact with each other
1. Determine which physics bodies within the scene intersect with points, rectangles, or rays


**Properties:** <br />
1. Gravity.
2. Speed

**Joining physics bodies:** <br />
```Swift
func addJoint(_ joint: SKPhysicsJoint)
```

**Detect collisions :**
```Swift
unowned(unsafe) var contactDelegate: SKPhysicsContactDelegate!
```
