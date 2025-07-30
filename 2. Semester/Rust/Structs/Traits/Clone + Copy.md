The trait clone allows Structs to implement the method: **clone()**
- this way we can create a copy of the data 


#### Implement Clone and Copy
- this would work the same as clone (creates a replica of the data)
- but there is no need of calling it explicitly 
	- functions that consume ownership of a datatype that implements Clone and Copy will use a copy of that data

```Rust

#[derive(Debug, PartialEq, Clone, Copy)]
pub struct WrappingU32 {
	value: u32,
}
  
impl WrappingU32 {
	pub fn new(value: u32) -> Self {
		Self { value }
	}
}
 
use core::ops::Add;
impl Add for WrappingU32{
		type Output = Self;
		fn add(self, other: Self)->Self::Output{
		Self{value: self.value.wrapping_add(other.value)}
	}
}

#[cfg(test)]
mod tests {
	use super::*;
	#[test]
	fn test_ops() {
		let x = WrappingU32::new(42);
		let y = WrappingU32::new(31);
		let z = WrappingU32::new(u32::MAX);
		assert_eq!(x + y + y + z, WrappingU32::new(103));
	}
}
```

# String does NOT implement Copy
- otherwise it would create two pointers to the same "content"
	- which would cause **double ownership**
- Strings must be called explicitly with: **clone()**