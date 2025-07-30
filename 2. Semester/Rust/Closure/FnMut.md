### Borrows mutable values from external scope
```Rust
fn main() {
	let mut x = 5;
	println!("x before calling closure = {}", x);

	// modifies x (thanks to mut my_closure)
	let mut my_closure = |input| x += input;
	my_closure(10);
	println!("x after calling closure = {}", x);
}
```