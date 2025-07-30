#### consumes the iterator and applies the closure to each element 

```Rust
fn main(){

	let mut collction = Vec::new();
	collction.push(1);
	collction.push(2);
	collction.push(3);
	
	collction.iter().for_each(|num| println!("{}", num));

}
```