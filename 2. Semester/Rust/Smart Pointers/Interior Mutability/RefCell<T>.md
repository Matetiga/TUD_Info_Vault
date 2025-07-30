#### Allows (inside) data to be mutable even if RefCell is immutable
- 
- <span style="color:#ffff00">borrowing rules are checked at runtime</span>
---
### Use
- to bypass rust ownership control
	- and there is **shared ownership and references need to mutate the data** 
	- there can *not be two (or more)* <span style="color:#ffff00">mutable references</span> to a value in the same scope
	- there can be **multiple borrows** but <span style="color:#ffff00">not if there is</span> an active **mutable borrow**
---
Mutable memory location
- Borrow rules are checked dynamically (panics if borrow rules are violated)
- uses lifetimes
---
## Methods:
- **borrow()**
- **borrow_mut()**
---
### Advantages over [[Cell<T>]]
- can <span style="color:#ffff00">handle Non-copy</span> and large types

---
### Check current borrow state
- try_borrow()
- try_borrow_mut()

```Rust
use std::cell::RefCell;

fn main() {
	let a = RefCell::new("Rust");
	println!("A: {:?}" , a.try_borrow ().is_err());
	let b = a.borrow();
	println!("B: {:?}" , a.try_borrow ().is_err());
	drop(b); // If we do not drop the borrowed reference, we’ll receive an error
	let _c = a.borrow_mut ();
	println!("C: {:?}" , a.try_borrow ().is_err());
}
```
```txt
A: false
B: false
C: true
```

---

## Change data

```Rust
let a = RefCell::new("Rust");
{
	let mut b = a.borrow_mut();
	*b = "Rust Lecture";
}
println!("{a:?}");
```

#### Or

```Rust
let a = RefCell::new("Rust");
a.replace("Rust Lecture");
println!("{a:?}");
```