##### It is used to convert one data type into another

## static_cast
- compiler-time type conversions
- implicit conversions between compatible types:
int => float
pointer => base class or derived class

```cpp
#include <iostream>

int main() {
    // Example 1: Converting numeric types
    double d = 3.14159;
    int i = static_cast<int>(d); // Convert double to int
    std::cout << "d = " << d << ", i = " << i << std::endl;

    // Example 2: Converting pointers
    int value = 42;
    int *ptr = &value; // Pointer to an integer
    void *voidPtr = static_cast<void*>(ptr); // Convert int* to void*
    std::cout << "Value pointed to by voidPtr: " << *(static_cast<int*>(voidPtr)) << std::endl;

    return 0;
}
```