```Rust
struct SingleType <T> {
	x: T,
	y: T,
}
// this can accept multiple datatype parameters
struct MultiType <T, U> {
	x: T,
	y: U,
}

impl<T> SingelType<T>(){
...
}
```

Not every value inside of the struct has to be `T` (**it can also be a fixed datatype**)
```Rust
struct Point<T> {
	x: T,
	y: T,
	//Internally, compiler transforms
	//generic deﬁnition into actual types
}
fn main() {
	let p_int = Point::<u32> { x: 5, y: 10 }; // Type: Point_U32
	let p_float = Point { x: 1.0, y: 4.0 };// Type: Point_F64
	let p_char = Point { x: '7', y: '3' };// Type: Point_Char
	
	println!("{:?}", p_int);
	println!("{:?}", p_float);
	println!("{:?}", p_char);
}
```