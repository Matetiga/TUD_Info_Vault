```cpp
#include <iostream>
#include <cmath>

struct Testing{
	float x;
	float y;
	float z;
	float betrag(){
		return sqrt(x* x + y*y + z*z);
	}
};

int main(){
	Testing test_1;
	test_1.x = 10;
	test_1.y = 2;
	test_1.z = 7;
	std::cout << "This is the value " << test_1.betrag()<< std::endl;

}
```