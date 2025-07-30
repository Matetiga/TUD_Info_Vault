*define an array of generic vertex attribute data*
- [doc](https://docs.gl/gl4/glVertexAttribPointer)
- Tells OpenGl the layout of the Buffer
## Enable Condition 
glEnableVertexAttribArray(0);


---

## Description

### Normalized 
- for example for Color (int between 0 and 255) will be normalized to 1 and 100
### Pointer 
- Is the offset that is needed to access the different attributes of a [[Vertex]]
- If in the Buffer there are multiple Vertizes stored (each with multiple attributes), then the offset will be the lenght of each attribute 
	- Example: 
	- Position is stored in the 11 first bits of the Buffer -> Offset = 0
	- Texture Coordinate is stored between the 12 and 19 bit -> Offset = 12
	- Normal is stored between the 20 and 32 bit -> Offset = 20

### Stride
- Amount of Bits between [[Vertex]]
- If each Vertex is 32 bit long,
	- then to go to the next Vertex -> Stride = 32;


---

## Example
```cpp
    float position[6] = {
        -0.5f, -0.5f,
        0.0f, 0.5f,
        0.5f, -0.5f
    };
    
    unsigned int buffer;
    glGenBuffers(1, &buffer);
    glBindBuffer(GL_ARRAY_BUFFER, buffer); 
    glBufferData(GL_ARRAY_BUFFER, 6 * sizeof(float), position, GL_STATIC_DRAW); 

	// the following lines will tell OpenGL the structure of the layout of the buffer
    glEnableVertexAttribArray(0);
    // 2 * sizeof(float) = the amount of bits to go to the next Vertex
    glVertexAttribPointer(0, 2, GL_FLOAT, GL_FALSE, 2 * sizeof(float), 0);
```