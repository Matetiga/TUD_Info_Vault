## Use 
```cpp
#include <iostream>
using namespace std;
// Inline function
inline int square(int x) { 	return x * x; }  

int main() {
	int num = 5; 	 	
	int res = square(num); // Calling inline function 	
	cout << res;
	return 0;
}   
```
- the **code** in the main function will be **substituted** with the one in the **inline function**
- there are no jumps across memory locations (e.g. if the function was a normal function)
### Important
- Is only useful to make the function inline if the **time spent during a function call is more compared to the function body execution time**

---
## Need
When a function is called, the CPU stores the return address, copies arguments to the stack, and transfers control to the function. After execution, the return value is stored, and control is returned to the caller.
This overhead can be significant for small, frequently used functions, as their execution time is less than the time spent on the call and return process