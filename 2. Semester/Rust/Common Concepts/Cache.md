Values will be stored in a HashMap in order to avoid computing them
- Example: Fibonacci
	- if we need constantly to compute values using the fibonacci sequence
	- if we constantly need the values for n <= 20
	- we could compute the sequence for n = 20 (for example)
	- and then store each value into a hashmap 
		- when we need again a value 
		- we can search it in the hashmap 
		- and not recompute it 

```Rust
pub fn fibonacci_i(n: u64) -> u64 {
	// we cache the results in a hash map O(1) access time
	let mut fib_cache: HashMap<u64, u64> = HashMap::new();
	
	fn fi(n: u64, fib_cache: &mut HashMap<u64, u64>) -> u64{
	
	match n {
		0 => panic!("fibonacci not defined for argument 0!"),
		1 | 2 => 1,
		_ => match fib_cache.get(&n) {
		// value is stored in the hashmap
		Some(r) => *r,
		// value is not in the hashmap => calculate and store it
		None => { let r=fi(n-1, fib_cache)+fi(n-2, fib_cache);
		fib_cache.insert(n,r); r }
			},
		}
	}
	fi(n, &mut fib_cache)
}
```