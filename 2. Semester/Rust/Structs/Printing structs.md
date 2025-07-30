Using the debugger function (this only prints for the developer)
- {:#?} => prints the struct variables as a list
- {:?} +> prints the struct variables in a single line
```Rust

#[derive(Debug)]
struct Rectangle{
	width: i32,
	height: i32,
}

fn main(){
	let rect1 = Rectangle{
		width: 20,
		height: 50,
	}

	// 
	println!("{:?}", rect1);
}
```