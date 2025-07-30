All functions implemented inside an impl block
=> because they are <span style="color:#00ff04">associated</span> with the <span style="color:#00ff04">impl type</span> 

#### Structs are allowed to have multiple impl blocks and associated functions

### Called with =>    ::
but also like normal functions
```Rust
struct Rectangle{
	width: i32,
	height: i32,
}

impl Rectangle {
    fn square(size: u32) -> Self {
        Self {
            width: size,
            height: size,
        }
    }

	fn set_width(&mut self, width: i32){
		self.width = width;
	}
}

fn main(){


	let s = Rectangle::square(10);
  
	// this two lines are equivalent
	let new = s.set_width(2);
	let new1 = Rectangle::set_width(&mut s, 2);
	println!("{:?}", s);
}
```