## Lazy Evaluation
- computation of data is **delayed until that specific data is needed**
	- used in [[map()]] , [[filter()]] ...
```Rust
fn main() {
    let numbers = vec![1, 2, 3, 4, 5];
    
    // Create an iterator and apply the `map` function to it
    let iter = numbers.iter().map(|x| x * 2);
    
    // At this point, the map operation hasn't been executed yet; it's deferred
    // until we consume the iterator with a method like `collect`.
    let doubled_numbers: Vec<i32> = iter.collect();
    
    println!("{:?}", doubled_numbers); // Outputs: [2, 4, 6, 8, 10]
}

```


## Eager Evaluation
- operations are evaluated immediately 
	- results are stored right away
```Rust
fn main() {
    let x = 2 + 3; // The expression 2 + 3 is evaluated immediately
    println!("{}", x); // x is printed, and the value is 5
}

```
### another lazy example
```Rust
// PREGUNTA DEMASIADO BASADA
fn main() {
	let input = vec![1, 2, 3];
	  
	let parity = input
		.iter()
		.map(|x| {
		print!("-{}", x);
		x % 2
	});
	  
	for p in parity {
		print!("{}", p);
	}
}
```
