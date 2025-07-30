## There is exactly <span style="color:#ffff00">one owner</span> of a variable at any given time
#### [[Moving Ownership]]
### [[Cloning]]

### [[Stack - Heap]]

### [[Ownership at Compile Time]]

### [[Ownership - Mutating variables]]

---
## <span style="color:#00fbff">Move Heap data principle:</span>

If a variable *x* moves Ownership of heap data to another variable  *y*, then *x* **can not be used after the move

---

### Ownership is about safety of the code:
for let *a = Box::new(1);* we say: a owns the box. The statement *let b = a*, moves ownership of the box to **b**


### Undefined behavior
```Rust
fn main(){
	// note that ola is called to the function before it is defined
	// this will cause an error
	conditions(ola);
	let ola = true;
	
}

fn conditions(x: boolean){
	if x{
		pritnln!("it is true");
	}
	else{
		println!("sad");
	}
}
```
In assembly code the order can be moved in which functions and variables are called.

#### This causes undefined behavior
- a way to prevent this -> Rust checks undefined behavior *compile-time* instead of *run-time*


---

##### mut takes ownership of the variable 

