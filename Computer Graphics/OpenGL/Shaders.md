## Vertex Shader 
- for each Vertex
- determines the position of the [[Vertex]] on the screen
### Code
```glsl
#shader vertex
#version 330 core  
   
layout(location = 0) in vec4 position;  
   
void main()  
{  
    gl_Position = position;  
};

```

---

## Fragment Shader 
- calculates the color for eac pixel

### Code
```glsl
#shader fragment
#version 330 core  
   
layout(location = 0) out vec4 color; 

uniform vec4 u_Color;

void main()  
{
    color = u_Color;   // RGBA color 
};
```
#### Layout  - Explanation
`layout(location = 0) out vec4 color; `
- The `layout` qualifier specifies metadata about how the variable is handled by the OpenGL pipeline
- `location = 0` assigns the output variable to a specific **location index** (in this case, index 0). This index corresponds to a specific **framebuffer attachment** or **render target** in the OpenGL pipeline
	- When working with **multiple Outputs**: Each output needs a specifi location 
	- `location = 1` ...
- The `out` qualifier indicates that the variable color is an **output variable** from the fragment shader.
	- In a fragment shader, `out` variables typically represent the final color (or other data) of a pixel or fragment
This line indicates an output variable that will hold the end-color of a fragment 
#### Uniform - Explanation
- [[Uniform Variables]]

