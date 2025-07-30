[[Functions as parameters]]
```Rust

type Fi32 = fn(i32) -> i32;
fn function_return(selector: i32) -> Fi32 {
match selector {
		    //=> these are anonymous functions
		1..=3 => |a| a + 1,
		4..=5 => |a| a + 2,
		6..=7 => |a| a + 3,
		_ => |a| { a }
	}
}

fn main(){
	// returning a function
	println!("The result for function_return(3)(2)= {}", function_return(7)(2));
		println!("The result for function_return(5)(2)= {}", function_return(5)(2));
	
}
```