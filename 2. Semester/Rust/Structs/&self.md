- within an impl block => type <span style="color:#1fffc7">self is an alias for</span> the <span style="color:#1fffc7">type in the impl</span> block is for
- self is an equivalent for *this* in Java


- <span style="color:#ffff00">self</span>: to access the method's instances taking ownership
- <span style="color:#ffff00">&self</span>: reference to the instance, allowing methods to read them
- use <span style="color:#ffff00"> &mut self</span> => to change the <span style="color:#00ff04">instance</span> in which the method is called
(<span style="color:#00ff04">instance</span> is when crating a variable with the struct)


```rust
impl Point {
    // A method that modifies the instance it's called on
    fn move_by(&mut self, dx: f64, dy: f64) {
        self.x += dx;
        self.y += dy;
    }

    // A method that only needs to read the instance
    fn x(&self) -> f64 {
        self.x
    }

    // A method that consumes the instance
    fn drop(self) {
        // `self` is consumed, typically to release resources or similar
    }
}
```