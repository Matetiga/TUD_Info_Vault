#### Used for indicating return types or parameters
=> that are of the same type that of the structs


```rust
struct Point {
    x: f64,
    y: f64,
}

impl Point {
    // A method returning a new instance of the same type
    fn new(x: f64, y: f64) -> Self {
        Self { x, y }
    }

    // A method that takes another instance of the same type
    fn distance_to(self, other: Self) -> f64 {
        let dx = self.x - other.x;
        let dy = self.y - other.y;
        (dx*dx + dy*dy).sqrt()
    }
}
```