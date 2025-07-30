### iter()
```Rust
{
	let v1 = vec![1, 2, 3, 4, 5];
	for item in v1.iter() {
		// ... - Do something with the item
		// *item += 1; will crash -> Immutable
		println!("{:?}", item);
	}
}
```

## iter_mut()
- => iterate mutable references
```Rust
{
	let mut v1 = vec![1, 2, 3, 4, 5];
	for item in v1.iter_mut() {
		*item += 1;
		println!("{:?}", item);
	}
	println!("{:?}", v1);
}
```

### into_iter()
- takes ownership of iterated items
```Rust
{
	let v1 = vec![1, 2, 3, 4, 5];
	let v2 = v1.into_iter()
		.map(|item| item + 1)
		.collect::<Vec<_>>();
		
	println!("{:?}", v2);
}
```
---

### collect()
- stores the iterated elements in a new Vector