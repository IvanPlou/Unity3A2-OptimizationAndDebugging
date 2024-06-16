Unity 3 A2 OptimizationAndDebugging
by: Ivan Plouganou

Fixes:

- Hierarchy Organization:
   Lighting
   Camera
   AI
   World
   PoolSystem

- Lighting:
    Exposure settings in the Global Volume, changed Mode from fixed to automatic and increased max limit
    Fog settigns in the Gloabal Volume, changed the attenuation distance to 75
    Directional Light intensity reduced to 20000
    Directional light mode changed to Mixed
    World meshes settings changed to Static and Controbute to GI
    Probe Placement Spacing changed to 3m Min to 27m Max
    Global Refelection Probe Type changed from Realtime to Baked

- HealthBar Prefab
    Current component image type changed from Simple to Filled

- Console Warning
    MechAnimations script, typo in the animation parameter changed from "Sped" to "Speed"

- Console Error
    Projectile script, added a null check on the OnTriggerEnter single target damaged fallback.

- Wrong Pooling of Projectiles
    In the Weapon script, on the TryFire method, changed the Instantiate method to a PoolSystem.Instance.Get

- GC Alloc 
    In the Unit script, on the FindTarget method, changed the OverlapSphere method to OverlapSphereNonAlloc, changed the hitCount parameter signature to int type and use that parameter in the for loop.    


Issues:
- My game runs at around 45-50 fps even after all the fixes. I couldn't find any other problems yet