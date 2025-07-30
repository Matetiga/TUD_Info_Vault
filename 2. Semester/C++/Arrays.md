```cpp
const char s1[] = "Hola a todos"; // size is constant
double rect[4];
```
---

## Stack array
```cpp
int arr[4] = {1, 2, 3, 4};
```

---
## Heap array
```cpp
#include <vector>

int *arr = new int[10]
std::vector<int> vec{1,2,3,4};
//std::vector <int> vec(4) -> initialized vector size 4 without elements
vec.push_back(5)
```

```cpp
#include <iostream>

std::array<int, 4> arr = {1, 2, 3, 4};
```