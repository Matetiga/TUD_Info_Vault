Mutable memory location
### Suitable for datatypes implementing Copy

## Methods
● **get()** returns duplicated data
	○ For types implementing Copy
● **get_mut()** returns mutable reference to data
	○ Checked at compile-time
	○ Only works with self being mutable

● **set()** and **replace()** changing value
	○ Old value is dropped

● **into_inner()** unwraps data
	○ Cell is consumed

● **take()** returns value, sets cell to Default
	○ Similar to function in Option


```Rust
use std::cell::Cell;
fn main() {
	let c1 = Cell::new(5);
	println!("Data: {:?}", c1);
	c1.set(10);
	println!("Data: {:?}", c1);
	c1.replace(15);
	println!("Data: {:?}", c1);
	let c2 = c1.clone();
	let c3 = c2.take();
	println!("Data: {:?}", c1.into_inner());
	println!("Data: {:?}", c3);
	println!("Cell: {:?}", c2);
}
```
```txt
Data: Cell { value: 5 }
Data: Cell { value: 10 }
Data: Cell { value: 15 }
Data: 15
Data: 15
Cell: Cell { value: 0 }
```