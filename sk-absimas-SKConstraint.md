#SKConstraint

`SKConstraint`s are used to ensure certain node relations before rendering, such as its position or orientation.

After a scene processes actions and physics, it applies constraints to the nodes in its node tree.

##Methods

- positionX
Limit the X axis
- positionY
Limit the Y axis
- orientToPoint
The node will rotate around a specific point
- orientToNode
The node will rotate around a specific node

General example:

```Swift
let node = SKNode()
var constraints = [SKConstraint]()

// X from 0 to 10
constraints += [SKConstraint.positionX(SKRange(lowerLimit: 0, upperLimit: 10))]
// Y from -10 to 0
constraints += [SKConstraint.positionY(SKRange(lowerLimit: -10, upperLimit: 0))]

node.constraints = constraints
```

##Properties

- enabled : Bool

Specified if the constraint is enabled