
## Move Heap data principle:

If a variable *x* moves Ownership of heap data to another variable  *y*, 
then *x* **can not be used after the move

---

![[Screenshot from 2024-04-22 19-44-59.png]]

#### first cannot be used because ownership of the heap has been transferred to full!!!!!

---
### This file will NOT compile
Rust checks **ownership at compile-time NOT run-time**
```Rust
fn main() {
  let s = String::from("hello");
  let s2;
  let b = false;
  if b {
	 s2 = s;
  }
  println!("{}", s);
}
```