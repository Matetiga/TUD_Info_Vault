## Implementation
```Rust
// impl<T> Type<T>
impl<T> Point<T> {
	fn swap(self) -> Point<T> {
		Point::<T> {
		x: self.y,
		y: self.x,
		
		}
	}
}
```