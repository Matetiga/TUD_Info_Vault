## if is an EXPRESSION
- the condition must be a boolean
- the condition does not need to be in klammern
- 
```Rust 
fn main(){
	// the condition has to be a boolean (1 and 0 don't work)
	if condition {
		println!("The condition evaluates tp true");	
	}
	
	// if are expressions, therefore they don't need a semicolon
	let y = if true{2} else {32};
}
```

### Expressions in if-arms must be of the same type
```Rust
fn main(){
	let x = if condition{2} else{"Error"};

}
```




#### These two snippets output the same result
```Rust
Snippet 1:
let x = if cond { 1 } else { 2 };

Snippet 2:

let x;
if cond {
  x = 1;
} else {
  x = 2;
}
```