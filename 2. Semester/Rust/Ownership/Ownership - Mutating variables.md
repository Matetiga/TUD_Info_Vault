#### Mutating an immutable reference is NOT GOOD

```Rust
fn main() {
	let mut s = String::from("Hello");
	let s_ref = &s;

	// s_ref does not have the write permission
	// only read permission
	s_ref.push_str(" world");
	println!("{s}");
}
```

#### Mutating a immutable borrowed data is NOT GOOD
```Rust
fn main() {
	let mut s = String::from("Hello");
	// s_ref is immutable
	let s_ref = &s;

	// s is changed to Read only permission
	s.push_str(" world");
	println!("{s_ref}");
}
```


### Mutating a mutable reference is GOOD
```Rust
fn main() {
	let mut s = String::from("Hello");
	let s_ref = &mut s;
	s_ref.push_str(" world");
	println!("{s}");
}
```