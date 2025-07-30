- [[FnOnce]]
- [[FnMut]]
- [[Fn]]
## Characteristics:
- anonymous functions
- can <span style="color:#ffff00">access variables outside</span> of its scope
- <span style="color:#ffff00">input/output type</span> can be ignored

---

### are defined with: |  |
```Rust
|param1: type, param2, type, ...|{
	// Implementation
}
```

---

#### Example:
```Rust
fn main() {
	let x = 10;
	let my_closure = |input: i32| {
		x + input
};
	println!("closure output: {}", my_closure(5));
}
```