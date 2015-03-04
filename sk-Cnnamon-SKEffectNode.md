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
	
	- Provide: two sprites that provide lighting information

	- What it does: effect node accumulates the effects of these lights

	- Result: image has a blur filter on it
	
    ```Swift
    import SpriteKit

    var lightingNode = SKEffectNode()
    var lightTexture = SKTexture(imageNamed: "") //specify image
    var light = SKSpriteNode(texture: lightTexture)
    light.blendMode = .Add
    lightingNode.addChild(light)

    var blurFilter = CIFilter (name: "") // specify filter

    lightingNode.filter = blurFilter

    lightingNode.blendMode = .Multiply
    ```


	
* Scenes are effect nodes:

	- SKScene is a subclass of SKEffectNode
	
	- This means that deny scene can apply a filter to its contents

	- Beware, it can be expensive (not well designed for interactive effects)

* Keeping cache may improve performance of static content (shouldRasterize = true)

* Some properties:

    - CoreImage filter
    ```Swift
    var filter: CIFilter? 
    ``` 
    - YES - apples filter and blends results, NO (default) - rendering normally
	```Swift 
    var shouldEnableEffects: Bool 
```
	
	