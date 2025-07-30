## Trait `#[derive(PartialEq)]`
- With the keyword `derive` we can Implement a specific trait to a Struct (whose attributes are supported to implement that trait)
```Rust
use std::cmp::PartialEq;
struct Ticket {
	title: String,
	description: String,
	status: String,
}

// TODO: Implement the `PartialEq` trait for `Ticket`
impl PartialEq for Ticket {
	fn eq(&self, other: &Self) -> bool {
	self.title == other.title && self.description == other.description && self.status == other.status
} 
fn ne(&self, other: &Self) -> bool {
	if self.title != other.title{
		return true;
	}
	if self.description != other.description{
		return true;
	}
	if self.status != other.status{
		return true;
	}
	return false;
	}
}
```
## Works the same as
- PartialEq can be applied to the struct, because all its elements **(Strings) implement the trait PartialEq**
```Rust

#[derive(PartialEq, Debug)]
struct Ticket {
	title: String,
	description: String,
	status: String,
}
```