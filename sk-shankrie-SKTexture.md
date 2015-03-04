# SKTexture

SKTexture object manages the texture data and graphics resources needed to render the image. Once created, a texture object’s contents are immutable.

Loading and preparing texture data is expensive so SprietKit defers these actions and provides methods to control it.

Important methods:
* +textureWithImageName: - creates SKTexture object from an image file
* +textureWIthImage: - creates SKTexture from an inage object

Important properties:
```swift
var filteringMode: SKTextureFilteringMode
func size() -> CGSize
```

Declaration example:
```swift 
convenience init!(imageNamed name: String)
```


