- Methods input parameter must implement [[FnOnce]]
- Input parameter can be a **function or closure**

If **value**, we call this method on, is **None**:
- <span style="color:#00ff04">None is returned</span>
If **value** is **Some**:
- <span style="color:#00ff04">Reference to value inside Some</span> is given as input to function 

In this code, filter uses a boolean 
- if **true**: filter retains the value and returns **Some value**
- if **false**: filter drops the value and **returns None**
```Rust
fn less_than_ten(number: &i32) -> bool {
	*number < 10
}
fn main() {
	let wrong_value = Some(50);
	println!(
	"wrong_value after filtering: {:?}",
	wrong_value.filter(less_than_ten)
	);
	let desired_value = Some(5);
	println!(
	"desired_value after filtering: {:?}",
	desired_value.filter(less_than_ten)
	);
}
```
```txt
Output:
wrong_value after filtering: None
desired_value after filtering: Some(5)
```