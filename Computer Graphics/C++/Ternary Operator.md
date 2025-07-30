## ?:
- used as a simple if-else statement to assign values 
- *condition* ? *expression_if_true* : *expression_if_false
- if l1 is  nullptr  the condition evaluates to false 
	- x = 0;
- if l1 is not a nullptr the condition evaluates to true 
	- x = l1->val;
```cpp
// l1 and l2 pointers
int x = l1 ? l1->val : 0;
int y = l2 ? l2->val : 0;
```