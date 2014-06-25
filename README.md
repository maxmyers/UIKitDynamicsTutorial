UIKitDynamicsTutorial
=====================

## 6 Kinds of Animation Behaviors Effects

### UICollisionBehavior | UIDynamicItemBehavior | UIGravityBehavior | UIPushBehavior | UISnapBehavior | UIAttachmentBehavior

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
# UIPushBehavior
# UISnapBehavior
# UIAttachmentBehavior
