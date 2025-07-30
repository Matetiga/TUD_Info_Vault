Sums the values inside an iterator

```Rust
fn main() {
	let vec: Vec<u16> = (1..=10).collect();

	// for this sum() must be called with a type annotation
	// because the compiler can not inferr the type of the sum
	// if that operation would be outside the print statement, it would inferr its type
	println!("the sum of the elements is {}", vec.iter().sum::<u16>());
```

```Rust
fn main() {
	let vec: Vec<u16> = (1..=10).collect();
	let sum = vec.into_iter().sum(); 
	
	println!("the sum of the elements is {}", sum);
```