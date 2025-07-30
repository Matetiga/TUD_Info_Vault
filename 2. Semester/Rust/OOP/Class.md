### Implements
#### Constructor 
- Blueprint for creating for creating objects 

#### methods 
- for the objects

```Rust
pub struct Point {
	x: i32,
	y: i32,
}
impl Point {
	pub fn new(x: i32, y: i32) -> Self {
		Self { x, y }
	}
	pub fn x(&self) -> i32 {
		self.x
	}
	…
}
```