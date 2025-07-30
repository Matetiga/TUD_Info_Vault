
### [[Shadowing variables]]

#### Using let or [const](obsidian://open?vault=Coding%20VsCode&file=2.%20Semester%2FRust%2FConstants)



---

## if a variable is not going to be used (like python)
it can be replaced with: _

 ---
 
 Once they have been assigned a value, the value <span style="color:#ffff00">won't</span> change (by default)

### MUT 
makes variables to be mutable 
mutable variables can <span style="color:#00ff04">not change its datatype</span>
```Rust
let apples = 2; // immutable
let mut bananas = 5; // mutable
```

#### [[Constants]] CAN'T be mutable!!

---

### Print variables with println!
```Rust
let x = 1;
let y = 10;

println!("x = {x} and y + 2 = {}", y +2);
// prints: 
// x = 1 and y + 2 = 12
```

---
### Underscore
<span style="color:#ffffff">is a catchall value</span> 
```Rust
let guess: u32 = match guess.trim().parse() {
// only numbers are accepted
Ok(num) => num,
// underscore is a catchall value
Err(_) => continue,
```
if guess is not a number, Err( _ ) will be active