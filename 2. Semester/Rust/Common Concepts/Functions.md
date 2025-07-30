## [[Borrowing - Maintain ownership after a function]]

[[Anonymous functions]]
[[Functions as parameters]]
[[Returning functions]]
## Declaring functions:
Other functions can be defined **after or before** main

- The variable type must be called inside the function's signature
-  **Statements**:  instructions that perform an action without returning a value
- Statements end with a "coma", 

- **Expressions**: evaluate to a resultant value
- expressions don't end with a coma

```Rust
fn main(){
	myfunction(3);
	let x = five();
}

fn myfunction(x: i32) {
	println!("hola");
	let y = 1; 
	{
		// this is an statement
		let x =2;
		// this is an expression
		x+2
	}
	println!("{y}");
}
// returns an interger of 32 bits
fn five(a: i32)->i32{
	5
}
```


---


## Useful functions:
#### [[getting user input]]

---

## [[Returning multiple values]]
