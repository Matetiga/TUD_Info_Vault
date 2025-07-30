### we can avoid transferring ownership after we call a function using a variable if we <span style="color:#00fbff">use a tupe</span> 

```Rust
fn calculate_length(s: String) -> (String, usize) {
	let length = s.len();
	(s, length) // We return a tuple here
}
fn main() {
	let s1 = String::from("Hello");
	let (s2, len) = calculate_length(s1);
	println!("The length of '{}' is {}.", s2, len);
}
```


##### Using [[Tuples]]
```Rust
fn more_values(x: String)->(String, usize){
	let length = x.len();
	(x, length) // this two values are returned
}
```
