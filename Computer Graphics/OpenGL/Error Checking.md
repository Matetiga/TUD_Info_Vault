## Function
- Inside the second Macro
	- `#x` will transform the function into a string
	- `__FILE__, __LINE__` will pass the file_name and the Error line 
```cpp
#define ASSERT(x) if (!(x)) __debugbreak();
#define GLCall(x) GLClearError();\
    x;\
    ASSERT(GLLogCall(#x, __FILE__, __LINE__))

static void GLClearError() {
    while (glGetError() != GL_NO_ERROR);
}

static bool GLLogCall(const char* function, const char* file, int line) {
    while (GLenum error = glGetError()) {
        std::cout << "[OpenGl Error] --> (" << error << ") function: "<< function << " file : " << file <<
            " on line : "<< line << std::endl;
        return false;
    }
    return true;
}
```

- This should be called before each function call
```cpp
GLCall(glDrawElements(GL_TRIANGLES, 6, GL_INT, nullptr));
```