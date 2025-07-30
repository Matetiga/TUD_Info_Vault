clones the heap bound to a variable
![[Pasted image 20240422195326.png]]
#### this makes that first can be used by println!()
without this line: 
```Rust
let first_clone = first.clone();
```
we would get an compile error, because ownership would have been transferred to full 
=> that would have made that first to lose its pointer to the heap