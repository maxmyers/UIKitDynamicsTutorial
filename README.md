UIKitDynamicsTutorial
=====================

## 6 Kinds of Animation Behaviors Effects

### UICollisionBehavior | UIDynamicItemBehavior | UIGravityBehavior | UIPushBehavior | UISnapBehavior | UIAttachmentBehavior

## Animations
###UIGravityBehavior = Movements like being pushed by gravity
###UIPushBehavior = Push movement
###UISnapBehavior = Snap Movement

## Animation Settings
###UICollisionBehavior = Add ability for animation item to collide. 
###UIDynamicItemBehavior = Add ability to change animation settings
###UIAttachmentBehavior = add attachment behavior


## Example Of Animation Behavior

`
@property (nonatomic,strong)UIDynamicAnimator*animator;
`

  ```objective-c
    self.animator=[[UIDynamicAnimator alloc]initWithReferenceView:self.testView];
    UIGravityBehavior *gravityBehavior = [[UIGravityBehavior alloc] initWithItems:@[self.testView]];
    [self.animator addBehavior:gravityBehavior];
```

### 1. Add UIDynamicAnimator Property To Class
`
@property (nonatomic,strong)UIDynamicAnimator*animator;
`

### 2. Initialize UIDynamicAnimator
  ```objective-c
self.animator=[[UIDynamicAnimator alloc]initWithReferenceView:self.view];
```
### 3.  Choose which view/views to add effects to and Choose animation Behavior
  ```objective-c
 //UIAttachmentBehavior, UICollisionBehavior, UIDynamicItemBehavior, UIGravityBehavior, UIPushBehavior, UISnapBehavior
UIGravityBehavior *gravityBehavior = [[UIGravityBehavior alloc] initWithItems:@[WhatEverViewYouWant1,WhatEverViewYouWant2]];
```

### 4. Add Animator Behavior To UIDynamicAnimator
```objective-c
      [self.animator addBehavior:gravityBehavior];
  ```


# UICollisionBehavior

### Creates behavior that allows items to collide

  ```objective-c
    // Initialize UIDynamicAnimator
    self.animator = [[UIDynamicAnimator alloc] initWithReferenceView:self.view];
    
    // Create some sort of movement behavior that will allow object to move to show collision behavior
    UIGravityBehavior *gravityBehavior = [[UIGravityBehavior alloc] initWithItems:@[self.myView]];
    
    // Create behavior for item
    UICollisionBehavior *collisionBehavior = [[UICollisionBehavior alloc] initWithItems:@[self.myView]];
    
    //
    UIDynamicItemBehavior* propertiesBehavior = [[UIDynamicItemBehavior alloc] initWithItems:@[self.myView]];
    propertiesBehavior.elasticity = 0.75f;
    
    
    collisionBehavior.translatesReferenceBoundsIntoBoundary = YES;
    
    
    [self.animator addBehavior:propertiesBehavior];
    [self.animator addBehavior:gravityBehavior];
    [self.animator addBehavior:collisionBehavior];
```


# UIDynamicItemBehavior

### Creates a setting to tweak other behaviors


# UIGravityBehavior
  ```objective-c
  UIGravityBehavior *gravityBehavior = [[UIGravityBehavior alloc] initWithItems:@[self.myView]];
    
    gravityBehavior.angle = 3*M_PI/2; // Angle at which Gravity pushes in | DOWN = M_PI/2 | RIGHT = M_PI | LEFT = 2M_PI or 0 | UP = 3(M_PI/2)
    
    gravityBehavior.magnitude = 30 // 30 points per second
    
    gravityBehavior.gravityDirection=CGVectorMake(.1, .12); // (Gravity Acceleration In X Direction, Gravity Acceleration In Y Direction) Measured in 1000 points / second²
```

### Angle

### Magnitude

### GravityDirection

# UIPushBehavior
# UISnapBehavior
# UIAttachmentBehavior
