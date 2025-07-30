## MVP Matrix
### Model Matrix
The model matrix transforms vertices from _model space_ to _world space_
- The Geometry and meshes are defined in the model space 
$M = T \cdot R \cdot S$
- T : Transform
- R : Rotation 
- S : Scale
### View Matrix
Renderable objects, lights, and cameras all exist within the *world space*
- all vertices must be defined relatively to the camera.
_Camera space_ is the coordinate system defined as the camera at *(0,0,0)* facing down its Z axis. The camera also has a model matrix defining its position in world space. The inverse of the camera's model matrix is the _view matrix_, and it transforms vertices from _world space_ to _camera space_, or _view space_

$V= C^{-1}$
- V : View Matrix
- C : Camera Matrix
$v_{camera}= V \cdot  M \cdot v_{model}$

### Projection Matrix
Once vertices are in _camera space_, they can finally be transformed into _clip space_ by applying a projection transformation

$v_{clip} = P \cdot V \cdot M \cdot v$
#### Types of Projection
- Perspective projection results in the natural effect of things appearing smaller the further away they are from the viewer
- Orthographic projections do not have this feature, which can be useful for technical schematics or architectural


Once the vertex shader finishes and the clip space position is known, the pipeline automatically performs perspective division, dividing the :
- default value of $w_{clip}=1$
$$
\begin{bmatrix}
x \\
y \\
z
\end{bmatrix}
= 
\begin{bmatrix}
\frac{x_{clip}}{w_{clip}}\\
\frac{y_{clip}}{w_{clip}}\\
\frac{z_{clip}}{w_{clip}}
\end{bmatrix}
$$