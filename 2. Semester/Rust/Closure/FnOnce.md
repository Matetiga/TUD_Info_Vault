### Closures that can only be used once
```Rust
fn main() {
	let mut my_vector = vec![1, 2, 3];
	println!("x before calling closure = {:?}", my_vector);

	// this closure (with move) takes ownership of the vector
	let mut my_closure = move |input| my_vector.push(input);
	my_closure(10);
	println!("x after calling closure = {:?}", my_vector);
}
```