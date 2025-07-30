- Gives the compiler the option to dereference any Value that implements the trait *Deref* and not `&`

```Rust
struct MyBox<T>(T);

impl <T> MyBox<T>{
	fn new(x: T)-> MyBox<T>{
		MyBox(x)
	}
}

use std::ops::Deref;

impl<T> Deref for MyBox<T> {
    type Target = T;

	// implementing a method to make MyBox dereferenceable
	// dereference with => *
    fn deref(&self) -> &Self::Target {
    // returns the first value of the tuple
        &self.0
    }
}

```