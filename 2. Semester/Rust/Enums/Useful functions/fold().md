## is used like an iterator
-  the fold function is used to combine all elements of an iterator, using an initial value

 - it makes use of an accumulator and a closure

- the accumulator has the value that is returned and passed to the next iteration


### Example: Factorial function 
- accumulator stores the previous value and uses it for the next iteration of the closure
```Rust
pub fn factorial(num: u64) -> u64 {
	(1..=num).fold(1, |acc, x| acc * x)
}
```