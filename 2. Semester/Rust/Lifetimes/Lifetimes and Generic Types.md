## Using generics and lifetimes at the same time
- while implementing a function 

```Rust
fn test_func <'a, T: Debug> (x: &'a T)
```