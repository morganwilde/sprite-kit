# SKPhysicsJoint

An SKPhysicsJoint object connects two physics bodies so that they are simulated together by the physics world. You never instantiate objects of this class directly; instead, you instantiate one of the subclasses that defines the kind of joint you want to make.

Joint classes implemented in Sprite Kit:
1. SKPhysicsJointFixed 
2. SKPhysicsJointSliding
3. SKPhysicsJointSpring
4. SKPhysicsJointLimit
5. SKPhysicsJointPin

How to use:
Create 2 physics objects -> attach them to SKNode objecs -> create a joint object using one of the subclass above -> configure its properties -> add to scene.