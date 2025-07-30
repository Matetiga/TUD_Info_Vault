### Implementation
- Implement a struct to iterate over
- define: *type*
- define: *next()*

```Rust
struct Counter {
    count: u32,
    max: u32,
}
```

```Rust
impl Iterator for Counter {
    type Item = u32;

    fn next(&mut self) -> Option<Self::Item> {
        if self.count < self.max {
            self.count += 1;
            Some(self.count)
        } else {
            None
        }
    }
}

```