#### Reference to a sequence of elements in a collection
- it is used in  for [[Loops]]
```Rust 
fn main(){
	for number in 1..=5{
		println!("{number}");
		// prints from 1 to 5 included
	}
}
```
### Does not take ownership (it borrows)


---
## Operator: <span style="color:#ffff00">..</span> 
#### has a start value
- First index is 0
- can be omitted if we slice from beginning
#### has an end value
- <span style="color:#ffffff">Is exclusive</span> 
- inclusive if:    <span style="color:#ffffff">..=</span> 
- can be omitted if we slice until end


## Substrings with slices
```Rust
fn main(){
	let s = String::from("Hola buenas");
	let mut my_slice = &s[..4] // this borrows the until the fourth letter in the string s
}
```