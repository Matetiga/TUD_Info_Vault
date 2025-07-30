Rust does *not allow implementation* of traits to datatypes 
**That already implements that Trait in the standard library** 


```Rust
// This code does not compile
// PartialEq is already implemented for u32 in the standard library

impl PartialEq for u32 {
    fn eq(&self, _other: &Self) -> bool {
        todo!()
    }
}

```