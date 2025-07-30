If value it was called on, <span style="color:#ffff00">is None</span>:
- **output** will be the **input value** of the method

If value is of <span style="color:#ffff00">type Some</span>:
- **Value inside Some** will be returned

```Rust
fn main() {
	let none_value = None;
	println!("calling unwrap_or on None: {:?}", none_value.unwrap_or(10));
	let some_value = Some(5);
	println!("Calling or On Some Value: {:?}", some_value.unwrap_or(10));
}
```
```txt
Output:
calling unwrap_or on None: 10
Calling or On Some Value: 5
```