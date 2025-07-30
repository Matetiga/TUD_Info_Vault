- visibility to others with *pub*
- Keyword: *use*
- Access parent modules: *super*
- Defined with: *mod*

## Implementation
- Inline 
- separated files: *module.rs*
- separated directory
	- File *module.rs*
	- directory *module/(NEW)*



```Rust
mod colors {
	pub struct RGB{
		pub r: u8,
		pub g: u8,
		pub b: u8,
	}
}

mod something {
	pub use crate::colors::RGB;
}

fn main() {
	let rgb = crate::something::RGB{r: 255, g: 0, b: 0};
}
```