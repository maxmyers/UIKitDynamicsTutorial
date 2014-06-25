UIKitDynamicsTutorial
=====================

UIKitDynamics Tutorial

# Basic Animations

### 3 steps to basic animations

  ```objective-c
    self.animator=[[UIDynamicAnimator alloc]initWithReferenceView:self.testView];
    UIGravityBehavior *gravityBehavior = [[UIGravityBehavior alloc] initWithItems:@[self.testView]];
    [self.animator addBehavior:gravityBehavior];
```

##### 1. Create UIDynamicAnimator Property
`
@property (nonatomic,strong)UIDynamicAnimator*animator;
`

##### 2. Create UIDynamicAnimator Property
  ```objective-c
UIGravityBehavior *gravityBehavior = [[UIGravityBehavior alloc] initWithItems:@[WhatEverViewYouWant1,WhatEverViewYouWant2]];
```
