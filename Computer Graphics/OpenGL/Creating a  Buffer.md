```cpp
float position[] = {
    -0.5f, -0.5f, // bottom left   
    0.5f, -0.5f, // bottom rigth   
    0.5f, 0.5f,// top right        
    -0.5f, 0.5f, // top left       
};
unsigned int buffer;
glGenBuffers(1, &buffer);
glBindBuffer(GL_ARRAY_BUFFER, buffer); 
glBufferData(GL_ARRAY_BUFFER, 6 *2* sizeof(float), position, GL_STATIC_DRAW);
```

>[!Important]
>The Buffer **MUST** be of type *unsigned int* 

### Explanation
- glBindBuffer() :  binds a buffer object to the specified buffer binding point
- glBufferData() :  **size** will be in bytes (that is why is *multiplied by float*)

## Index Buffer
>[!Importance]
>to avoid re rendering the same vertex twice
```cpp
unsigned int indices[]{ // ANY INDEX BUFFER must be UNSIGNED
    0, 1, 2,
    2, 3, 0
};
unsigned int ibo; // index Buffer Object 
glGenBuffers(1, &ibo);
glBindBuffer(GL_ELEMENT_ARRAY_BUFFER, ibo);
glBufferData(GL_ELEMENT_ARRAY_BUFFER, 6 * sizeof(unsigned int), indices, GL_STATIC_DRAW); 
```

inside of the while loop (rendering loop)
- NOT forget : *GL_UNSIGNED_INT* 
```cpp
glDrawElements(GL_TRIANGLES, 6, GL_UNSIGNED_INT, nullptr);
```