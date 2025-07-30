Functions can be parameters of other functions
```Rust
  

fn apply<F>(func: F, arg: i32) -> i32
where
F: Fn(i32) -> i32,
{
	func(arg)
}

fn square(x: i32) -> i32 {
	x * x
}
 
fn main() {
	let result = apply(square, 5);
	println!("The result is: {}", result);
	let result = apply(|a| a+1, 5);
	println!("The result is: {}", result);

}
```


## 2. Example:
```Rust
fn main() {
	let func_place_holder = less_than_ten ;
	let result = another_function (20, func_place_holder );
	println! ("result: {}", result);
}

fn less_than_ten (number: &i32) -> bool {
	*number < 10
}

fn another_function (number: i32, func: fn(&i32) -> bool) -> bool {
	func(&number)
}
```