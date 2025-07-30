primitive data types:
- [[Strings]]
- boolean
- char <span style="color:#ffff00">(specified with sigle coutes)</span>

---

#### Intergers have the copy- trait
This means that when you pass a variable of a `Copy` type into a function or assign it to another variable, the **original value is still usable after the operation**

| unsigned interger       | signed interger         | float    |
| ----------------------- | ----------------------- | -------- |
| u8, u16, u32, u64, u128 | i8, i16, i32, i64, u128 | f32, f64 |
##### Signed intergers can store numbers in a specific range: $2^{n-1} \quad bis\ 2^{n-1}-1$

for example i8 => $2^{8-1}$ bis $2^{8-2}-1$  (so, -128 bis 127, because 0 is included)

##### Unsigned intergers range: $2^n$

```Rust 
fn main(){
	println!("i8 min value: {}", i8::min_value()); //-128
	println!("u128 max value: {}", u128::max_value()); // 340282366920938463463374607431768211455
}
```



---
## [[Tuples]] 

## [[Array]]

## [[Vectors]] 
### The (vector) size can grow and shrink