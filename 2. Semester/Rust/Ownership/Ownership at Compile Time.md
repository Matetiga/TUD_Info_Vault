## Variable permissions: 
## Read (R), Write (W), Own (O)
#### Own (O)
- there can Only be one owner at a time
- If two variables thought they own the same thing, both would try to deallocate it's space
#### Read (R)
- A reference changes the permissions of the variable to read only (not if is a mutable reference)
- a variable that is a pointer, does NOT OWN the data
#### Write (R)
- <span style="color:#ffffff">mut</span> => makes a variable obtain Write permission

---
### Variable permissions are changed if it is <span style="color:#ffff00">moved or borrowed</span> 

## Consuming ownership
```Rust
fn main() {
  let s = String::from("Hello world");
  consume_a_string(s);
  println!("{s}"); // can't read `s` after moving it
}

fn consume_a_string(_s: String) {
  // om nom nom
}
```

---

