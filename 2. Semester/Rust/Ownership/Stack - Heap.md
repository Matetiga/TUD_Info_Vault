### checks memory during COMPILE-TIME !!!

## Stack 
### <span style="color:#00fbff">stores data with a specific size</span>
- stores variables inside of stacks
- each **stack (data) lives only inside of a function** => after each function, the corresponding stack is <span style="color:#ffff00">deallocated</span> (*this means that memory is freed*)
---
## Heap 
### <span style="color:#00fbff">stores data, which size can not be calculated at compile-time (dynamic data)</span>
- uses pointers
- there can **only be one (mutable) pointer for each heap**
- <span style="color:#ffff00">heaps are deallocated</span> when the <span style="color:#ffff00">stack</span>, in which the variable that called the heap is, is <span style="color:#ffff00">deallocated</span> 
```Rust
fn main(){
	// this creates an array with 10 elements (number 1)
	// a is pointing to the heap
	let a = Box::new([1; 10]);
	let c = Box::new([2; 5]);

	// this changes the pointer from a to b to the heap
	let b = a
}
```

###### If a variable OWN heap data, then it CAN NOT be copied 
- String: owns heap data, it can not be copied
###### if a variable does NOT OWN heap data, it CAN be copied
- int, does not own heap data
- &String also don't own heap data

---
# Main difference between both forms of memory:
=> Stacks only live inside of functions whereas heaps can outlive them

---

### Freeing memory twice can lead to memory corruption