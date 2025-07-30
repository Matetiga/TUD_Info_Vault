- Creates a new *Some* value with a tuple if:
- Current value is *Some*
- Input is *Some*

```Rust
fn main() {
	let array1 = [-1, -2, -3, 0, 4];
	let mut first_positive = first_greater_than_zero(&array1);
	println!("first_positive value is: {:?}", first_positive);
	let zipped_value = first_positive.zip(Some(10));
	println!("zipped_value is: {:?}", zipped_value);
}
```
```txt
Output:
first_positive value is: Some(4)
zipped_value is: Some((4, 10))
```

