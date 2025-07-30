#### Are like functions, but they are implemented <span style="color:#ffffff">for a type</span> and only valid in it's context
- methods are defined within the context of a struct (or enum or trait object)
---
# [[&self]]
# [[Self]]
---
### Implementing a method
- with: <span style="color:#ffff00">impl</span>

```Rust
#[derive(Debug)]
struct Rectangle {
    width: u32,
    height: u32,
}

// everything with this block is related to Rectangle
impl Rectangle {
// self parameter
// self is short for => self: &Self
    fn area(&self) -> u32 {
        self.width * self.height
    }
}

fn main() {
    let rect1 = Rectangle {
        width: 30,
        height: 50,
    };

    println!(
        "The area of the rectangle is {} square pixels.",
        rect1.area()
    );
}
```


---
