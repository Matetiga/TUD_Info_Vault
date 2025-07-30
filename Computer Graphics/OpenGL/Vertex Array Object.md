The<span style="color:#ffff00"> VAO is a container</span> that holds the state of vertex attributes (e.g., which buffers are used, how data is formatted, and which attributes are enabled
- Can be created for each geometry form used 
- So the Information of how to store and read each Buffer will depend on the used form

## Example 
`glVertexAttribPointer` is what **binds buffer and vao together** 
- OpenGL links the currently bound VBO (*buffer*) to the vertex attribute (**index 0**) in the currently bound VAO (*vao*).
### Visualising the Code
It says, “For attribute 0, use the VBO `buffer`, read 2 floats per vertex, with a stride of 8 bytes, starting at offset 0
- The VBO is the “ingredient” (the actual data)
### Code 
```cpp
    unsigned int vao;
    GLCall(glGenVertexArrays(1, &vao));
    GLCall(glBindVertexArray(vao));

    unsigned int buffer;
    glGenBuffers(1, &buffer);
    glBindBuffer(GL_ARRAY_BUFFER, buffer);     
    glBufferData(GL_ARRAY_BUFFER, 4 *2* sizeof(float), position, GL_STATIC_DRAW); // size will be in bytes (that is why is multiplied by float)

    glEnableVertexAttribArray(0); // enables vertex attribute at index 0
    // IMPORTANT LINE 
    glVertexAttribPointer(0, 2, GL_FLOAT, GL_FALSE, 2 * sizeof(float), 0); // the first value (index) matches with the enabled vertex

```

#### Inside the rendering Loop
- We only have to bind the *vao* Buffer
```cpp
GLCall(glBindVertexArray(vao));
```