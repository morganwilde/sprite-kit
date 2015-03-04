# SKPhysicsJointSpring

SKPhysicsJointSpring object simulates spring physics between two physics objects.

Declaration example:
```swift 
class func jointWithBodyA(
    _ bodyA: SKPhysicsBody!,
    bodyB bodyB: SKPhysicsBody!,
    anchorA anchorA: CGPoint,
    anchorB anchorB: CGPoint) -> SKPhysicsJointSpring!
```

Properties:
```swift
var damping: CGFloat // (lit. slopinimas) defines that defines how the spring's motion should be damped (due to forces of friction)
var frquency: CGFloat // defines frequency characteristics of the spring
```