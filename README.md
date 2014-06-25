UIKitDynamicsTutorial
=====================

6 Kinds of Animation Behaviors UIAttachmentBehavior 

# UICollisionBehavior | UIDynamicItemBehavior | UIGravityBehavior | UIPushBehavior | UISnapBehavior

### 3 steps to basic animations

`
@property (nonatomic,strong)UIDynamicAnimator*animator;
`

  ```objective-c
    self.animator=[[UIDynamicAnimator alloc]initWithReferenceView:self.testView];
    UIGravityBehavior *gravityBehavior = [[UIGravityBehavior alloc] initWithItems:@[self.testView]];
    [self.animator addBehavior:gravityBehavior];
```

##### 1. Add UIDynamicAnimator Property To Class
`
@property (nonatomic,strong)UIDynamicAnimator*animator;
`

##### 2. Initialize UIDynamicAnimator
  ```objective-c
self.animator=[[UIDynamicAnimator alloc]initWithReferenceView:self.view];
```
##### 3.  Choose which view/views to add effects to and Choose animation Behavior
  ```objective-c
 //UIAttachmentBehavior, UICollisionBehavior, UIDynamicItemBehavior, UIGravityBehavior, UIPushBehavior, UISnapBehavior
UIGravityBehavior *gravityBehavior = [[UIGravityBehavior alloc] initWithItems:@[WhatEverViewYouWant1,WhatEverViewYouWant2]];
```

##### 4. Add Animator Behavior To UIDynamicAnimator
```objective-c
      [self.animator addBehavior:gravityBehavior];
    
  ```
