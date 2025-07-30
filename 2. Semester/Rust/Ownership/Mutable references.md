### mut takes ownership of the variable 

```Rust
fn main() {
	let mut v: Vec<i32> = vec![1, 2, 3];
	let num: &mut i32 = &mut v[2];
	//until this part, *num could read and write in v[2]
	
	let num2: &i32 = &*num;
	// until this part *num2 can only read (NOT write) *num

	println!("{} {}", *num, *num2);
}
```