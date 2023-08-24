# Investigation-on-Real-time-SDF-Generation-and-Utilizing-SDF-for-Collision-Detection

`VFX` `Signed Distance Fields` `Visual Effects Graphs` `Compute Shader` `Collision` `Boolean`

## Overview
Investigation on Real-time SDF Generation and Utilizing SDF for Collision Detection.


In pursuit of achieving continuous and real-time boolean operations, 
as well as soft real-time deformation and fracturing simulations in physics-based calculations, 
we embarked on investigating and validating an alternative approach based on 
signed distance functions for collision and boolean operations. 
This approach aimed to replace the original mesh-based representation scheme.

Regrettably, after several days of dedicated research, our efforts culminated in failure.
Nonetheless, the experiences gained are invaluable, warranting documentation for potential 
application in other avenues, such as soft tissue rendering.

My primary focus was on exploring methods and performance aspects of real-time signed distance 
function generation for model mesh, as well as techniques for generating mesh in real-time using 
signed distance functions (e.g., cube marching). Considering the additional challenge of 
real-time computation of normals and textures after mesh generation, 
I abandoned the path of re-generating grids from processed SDFs. 
Instead, I turned to Visual Effects (VFX) techniques to handle SDFs, 
leveraging particle rendering to achieve more favorable presentation outcomes.

Moving forward, I will elaborate on my research across several dimensions:

- Concept of Signed Distance Functions (SDFs)
- Real-time computation of SDFs for mesh and its performance implications
- Real-time generation of mesh from SDFs and associated performance considerations
- Collision between particles and SDFs
- Operations involving manipulation of SDFs

## Contents

### Concept of Signed Distance Functions

[SignedDistanceFunction](https://en.wikipedia.org/wiki/Signed_distance_function)

A Signed Distance Field (SDF) can be stored using various data structures such as a three-dimensional array, texture maps, or voxel grids. Each storage unit (pixel, voxel, etc.) holds distance information to the nearest object surface.

Constructing a Signed Distance Field can involve multiple methods, such as ray tracing, morphological operations, and distance field expansion. One common approach involves dilating or eroding an object's boundary and subsequently using distance field expansion algorithms to compute the distance from each point to the nearest object surface.

Signed Distance Fields are used for operations like shape blending, boolean operations, etc., facilitating geometric manipulations like merging and cutting.

Merging SDF Information: This involves combining the SDF information of two objects. A common merging technique is to select, for corresponding positions, the smaller absolute distance value from the two SDFs, which becomes the distance value in the merged SDF. This merged SDF incorporates distance information from both objects, reflecting the distance to the surfaces of the two objects at each point.


### Real-time computation of SDFs for mesh and its performance implications

[Mesh to SDF](https://github.com/Unity-Technologies/com.unity.demoteam.mesh-to-sdf)

[Mesh to SDF Samples](https://github.com/Unity-Technologies/com.unity.demoteam.mesh-to-sdf)

### Real-time generation of mesh from SDFs and associated performance considerations

There's so many repos for this like cube marching .

### Collision between particles and SDFs

[Collide With Signed Distance Field](https://docs.unity3d.com/Packages/com.unity.visualeffectgraph@12.0/manual/Block-CollideWithSignedDistanceField.html)

[Ray Marching and Signed Distance Functions](https://jamie-wong.com/2016/07/15/ray-marching-signed-distance-functions/)

[SDF VFX Samples(Unity tech.)](https://github.com/keijiro/SdfVfxSamples)


### Operations involving manipulation of SDFs

[A Repo. for Signed Distance Fields in Unity](https://github.com/samuelbigos/signed_distance_fields_in_unity)

[A Repo. for Vfx-Sdf-Collide](https://github.com/rainwl/VFX-SDF-DEMO.git)

### VFX tutorials

[Youtube Unity Visual Effect Graph Tutorials](https://www.youtube.com/watch?v=TwWL5IY4Lqs&list=PLQMQNmwN3FvySzk-SdqJeRa6hpH6FYKji)

[Youtube VFX Convert mesh to sdf](https://www.youtube.com/watch?v=Ujvel8WWoaM)

[Youtube SDF particle effects](https://www.youtube.com/watch?v=FBP9k6W48vM&t=153s)

[Youtube Intro of sdf](https://www.youtube.com/watch?v=pEdlZ9W2Xs0)

[Compute Shader](https://developer.unity.cn/projects/6116875dedbc2a00204564c9)

[Repo for compute shader](https://github.com/keijiro/NoiseBall2)

