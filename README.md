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

## Implement

### Collision between particles and SDFs





