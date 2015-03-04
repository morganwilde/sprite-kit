# SKMutableTexture

A texture that can be dynamically updated.

This class is used to manually alter sprites when this cannot be accomplished using other methods. At times when you need to change a specific texture, call `modifyPixelDataWithBlock:` method.

# Methods and examples

```Swift
init(size size: CGSize, pixelFormat format: Int32) // Designated initialiser
func modifyPixelDataWithBlock(_ block: (UnsageMutablePointer<Void>, UInt) -> Void) // Modifies each pixel
```
