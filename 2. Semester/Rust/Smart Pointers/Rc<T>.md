## Reference Counted
- enables <span style="color:#ffff00">multiple, shared</span> ownership
- **Data Mutation is forbidden**
- data can not be dropped as long as a single reference exists
- check number of references: *strong_count()*
- allows only immutable borrows

### usage
- it is useful to allocate data on the heap 
- and we don't know which part will be the last on using that allocated heap memory

```Rust
enum List {
	Cons(i32, Rc<List>),
	Nil,
}

use crate::List::{Cons, Nil};
use std::rc::Rc;

fn main() {
	let a = Rc::new(Cons(5, Rc::new(Cons(10, Rc::new(Nil)))));
	let b = Cons(3, Rc::clone(&a)); // Here, we could also call a.clone()
	let c = Cons(4, Rc::clone(&a)); // Does not deep-copy this time, uses Rc implementation
}
```
### Functions
- Rc::strong_count(&*variable*)=> used to count the number of pointers to a variable
- when this counter is 0 => value will be dropped


![[Screenshot from 2024-06-12 18-36-05.png]]