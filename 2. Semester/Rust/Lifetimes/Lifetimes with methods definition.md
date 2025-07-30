### When implementing a method for a struct that has a lifetime
```Rust
impl<'a> ImportantExcerpt<'a> {
    fn level(&self) -> i32 {
        3
    }
}

```
