#### requires a closure

```Rust
fn main() {
	let x: i128 = 13;
	let none_value = None;
	println!(
	"Calling or_else On None: {:?}",
	none_value.unwrap_or_else(|| x.pow(2))
	);
}
```
```txt
Output:
169
```