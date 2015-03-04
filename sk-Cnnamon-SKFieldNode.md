#SKFieldNode

Inherits from: SKNode : NSResponder : NSObject

##Summary

* A SKFieldNode applies physics effects to physics bodies within a specific part of the scene.

* Creating Field Nodes section lists the field types you can create using Sprite Kit, including a type that allows to apply custom forces to physics bodies.

* Instantiate the approptiate king of field node and then add ir to the scene's node tree.

* When the scene simulates physics effects, a field node applies its effect to a physics body so long as the following things are true:

    - The field node is in the scene’s node tree.

    - The field node’s enabled property is YES.

    - The physics body is attached to a node that is in the scene’s node tree.
    
    - The physics body is located inside the field node’s region (see region).

    - The physics body is not located inside the region of another field node whose exclusive property is set to YES.

    - A logical AND operation between the field node’s categoryBitMask property and the physics body’s fieldBitMask property results in a nonzero value.

##Methods and code examples

*Creating Field Nodes
- dragField: Creates a field node that applies a force that resists the motion of physics bodies.

```swift
class func dragField() -> SKFieldNode
```

- noiseFieldWithSmoothness:animationSpeed: Creates a field node that applies a randomized acceleration to physics bodies. Use a noise field to simulate effects such as fireflies or snow.

```swift
class func noiseFieldWithSmoothness(_ smoothness: CGFloat,
animationSpeed speed: CGFloat) -> SKFieldNode
```



