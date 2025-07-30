*(default types of closures)*

### Borrows immutable variables from external scope

```Rust
fn main() {
	let x = 10;
	let my_closure = |input| {
		x + input
	};
	println!("closure output: {}", my_closure(5));
}
```