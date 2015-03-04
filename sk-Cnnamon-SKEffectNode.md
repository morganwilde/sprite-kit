#SKEffectNode

Inherits from: SKNode : NSResponder : NSObject

##Summary

This node is used for adding some special effects into a scene or to cache the contents of a static subtree for faster rendering performance.

##What it does behind the scenes:

1. The effect node draws its children into a private frame buffer.

2. Applies Core Image effects. (optional: see filter and shouldEnableEffects)

3. Blends the private frame buffer into parents frame buffer.

4. Deletes private frame buffer. (optional: see shouldRasterize)

##Methods and code examples

* Example: Applying a Special Effect

	