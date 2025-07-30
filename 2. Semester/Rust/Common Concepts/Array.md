### The array size must be known before!!!
```Rust 
fn main(){
	let a = [1, 2, 3, 4, 5];

	let first = a[0];
	let second = a[1]'
}
```

## In order to create an array an fill it automatically
```Rust
fn main(){
	let a = [5; 10];
	// this creates an array of 10 elements
	// every number is 5
	
	let b = [i32; 10];
	// this creates an array with 10 elements
	// the elements have the i32 type
}
```