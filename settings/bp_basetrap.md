# BP\_BaseTrap

The function “**AnimationLogic**” needs to be redefined in successors, in it the logic of how the trap will be animated.

## Settings

* **TriggerRef** (BP\_BaseTrigger): reference on “_**BP\_BaseTrigger**_”

### **Animation**

* **DelayBetweenRepeat** (float): time in seconds between animations
* **NumberRepeatAnimation** (int): number of repetitions of animation if “_**bInfinityActivate**_” = false
* **bInfinityActivate** (bool): if true then the trap will work constantly, otherwise “_**NumberRepeatAnimation**_” repetitions will be done
* **bActiveTrap** (bool): activates a trap at the beginning of the game, if there is a link in the “_**TriggerRef**_” variable then “_**bActiveTrap**_” is set to false
* **DirectionAnimation** (E\_DirectionsAnimation): the direction of the animation, there are 3 positions:
  * forward and backward along the curve
  * forward along curve
  * back along curve
* **CurveVectorAnimation** (VectorCurve): the curve by which the trap is animated (more precisely, 3 curves). How much you decide to use. For example, along a curve X, motion is animated, and along Y, rotation.

### **DelayStart**

* **DelayStart** (float): delay in seconds before first trap activation
* **bRandomDelayStart** (bool): if set to true then a random value from “_**MinRandomDelayStart**_” to “_**MaxRandomDelayStart**_” will be set to “_**DelayStart**_”
* **MinRandomDelayStart** (float): minimum time in seconds
* **MaxRandomDelayStart** (float): maximum time in seconds

### **Damage**

* **Damage** (float): trap damage (writes damage in “_**BP\_BaseModularWeapon**_”)
* **bCustomImpulse** (bool): if set to true, “_**Impulse**_” will be used to repel otherwise “_**Impulse**_” will record the mesh speed
* **Impulse** (Vector3D): vector by which the character will repel if he has not died
* **DamageType** (Vector3D): when dealing damage, the type of damage is taken from this class (recorded through the trap)
