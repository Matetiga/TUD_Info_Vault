```Rust
struct Link<T> {
	data: T,
	next: Option<Box<Link<T>>>,
}
```
