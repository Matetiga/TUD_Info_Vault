If value, it was called on, is of *type Some*:
- returns Some part

If value is None:
- returns input parameter

```Rust
fn main() {
	let none_value = None;
	println!("Calling or() on none: {:?}", none_value.or(Some(5)));
	println!("Calling or() on none with None parameter: {:?}", none_value.or(None));
	let some_value = Some(5);
	println!("Calling or() on Some Value: {:?}", some_value.or(Some(10)));
}
```
```txt
Output:
Calling or() on none: Some(5)
Calling or() on none with None parameter: None
Calling or() on Some Value: Some(5)
```