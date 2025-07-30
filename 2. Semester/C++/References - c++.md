#### Works as an alias for a variable
##### once a reference is initialized with a variable, it behaves as if is that variable
- It is usually passed as a parameter to a function 
- which can alter the original variable 

```cpp
void addOne(int& i){
i = i +1;

}

int main(){
	int k = 0;
	addOne(k);
	// k is now => 1

	// 2. Example
	int x = 0;
	int y = 1;
	int &r = x;
	&r = y;

	// this will print 1 is the same as 1 \

	std::cout << x  << " is the same as " << r << std::endl;
}
```
###### Whatever you do to r (a reference) , will be made to x (the referenced value)
