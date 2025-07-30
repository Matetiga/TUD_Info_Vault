A Form to get Data from the CPU to the GPU
- **Used in the context of a Shader Program**


```cpp
// inside Basic.shader
uniform vec4 u_Color;
```
## Use
- **Read-only in the shader**: They are set by the application (e.g., your C++ code) and remain constant across all vertices or fragments processed by the shader during a single draw call.
- **Shared across the shader program**: Uniforms are global variables accessible in all stages of the shader pipeline (e.g., vertex, fragment shaders) where they are declared.
- **Used for external input**: They allow the application to pass data (like colors, matrices, or other parameters) to the shader. In this case, u_Color is a 4-component vector (vec4) likely representing a color (RGBA)

---
## Important
Uniforms are called for each *DRAW*
`glDrawElements(GL_TRIANGLES, 6, GL_UNSIGNED_INT, nullptr);`
- this function will draw two triangles (*second atributte is for 6 vertices*)
- both triangles will have the same color

