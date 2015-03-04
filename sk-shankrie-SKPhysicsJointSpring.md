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
var damping: CGFloat
var frquency: CGFloat
```