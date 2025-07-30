to change a (mutable) variable
#### [[Dereference]]

----
# rust compiler allows immutable reference and then mutable reference 
( to the same variable)

# rust compiler does NOT allow mutable and then immutable reference
----
#### A reference changes the permissions of the variable to read only (not if is a mutable reference)

## Are inmutable by default 
(this can be changed)

---
## Using &mut
- the start variable must be <span style="color:#ffffff">also mutable</span>


```Rust 
fn main(){
	let mut s = String::from("Una playita");
	modifier(& mut s);

	println!("s in the main function: {}", s);
}

fn modifier(input: &mut String){
	input.push_str("y unas bielitas"); //this is added at the end
}
```

---
## Multiple mutable references
There can only be <span style="color:#ffffff">1 !!</span> inside of a scope
```Rust
fn main(){
	let mut s = String::from("si");
	{
		let r1 = &mut s;
		
	} // r1 goes out of scope here

	let r2 = &mut s;
}
```

---
### References examples:

- ###### let r2: &i32 = &* x;  
=> this line makes r2 <span style="color:#1fffc7">point directly to the heap</span> an NOT to x
- * x: dereferences x (so r points to the heap)
- Then, & , creates a reference to an i32 value at the memory
```Rust
fn main() {
	let mut x: Box<i32> = Box::new(1);
	let a: i32 = *x;         // *x reads the heap value, so a = 1
	*x += 1;                 // *x on the left-side modifies the heap value,
	                         //     so x points to the value 2
	
	let r1: &Box<i32> = &x;  // r1 points to x on the stack
	let b: i32 = **r1;       // two dereferences get us to the heap value

	//this line is important
	let r2: &i32 = &*x;      // r2 points to the heap value directly
	let c: i32 = *r2;    // so only one dereference is needed to read it
}
```

---
## Explicit/Implicit References
```Rust
let x: Box<i32> = Box::new(-1);
let x_abs1 = i32::abs(*x); // explicit dereference
let x_abs2 = x.abs();      // implicit dereference
assert_eq!(x_abs1, x_abs2);

let r: &Box<i32> = &x;
let r_abs1 = i32::abs(**r); // explicit dereference (twice)
let r_abs2 = r.abs();       // implicit dereference (twice)
assert_eq!(r_abs1, r_abs2);

let s = String::from("Hello");
let s_len1 = str::len(&s); // explicit reference
let s_len2 = s.len();      // implicit reference
assert_eq!(s_len1, s_len2);

```