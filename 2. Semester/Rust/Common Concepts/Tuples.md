```Rust
fn main(){
	let tup: (i32, f64, u8) = (500, 6.4, 1);
}
```
Tuples values can be from <span style="color:#ffff00">different types</span>

### Access tuples values
```Rust
fn main(){
	let tup: (i32, f64, u8) = (500, 6.4, 1);

	// 1. Form
	let (x, y, z) = tup;
	println!("{x}"); // prints 500

	// 2. Form
	let five_hundred = tup.0;
	let six_point_four = tup.1;
	let one = tup.2;
}
```
---

### Tuples can be used to return multiple values
[[Functions]]