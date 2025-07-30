[[2. Semester/Rust/Ownership/References]]

## Using the * operator

```Rust
fn main(){

	let mut val = 42;
	let var_ref = &mut val;

	*val_ref = 27;

	println!("{}", val);
}
```


---

## Dereference coercion
- Rust compiler <span style="color:#ffffff">automatically dereferences</span> a variable as many times needed, **when called on a method**

