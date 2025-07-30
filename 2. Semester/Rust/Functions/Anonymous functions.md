[[Returning functions]]
[[Functions as parameters]]

Functions that can be called inline and don't have the syntax of a regular function

=> for example inside the [[find()]] method

```Rust
			//element is the variable 
			        //this is the anonymous function
v.iter().map(|element| {element * 2}).collect()
```