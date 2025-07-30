#### The scope of a variable ends, when it is used for the last time
#### Inside of a scope, there can <span style="color:#ffff00">only be one mutable reference
</span>
```Rust 
fn main(){

	let mut s: String = String::from("ola");

	let r1: &String = &s;
	let r2: &String = &s;
	// let r3: &mut String = &mut s;
	
	println!("{}, {}", r1, r2);
	//the scope of r1 and r2 ends with the println
	// this allows us to create a mutable reference to s
	let r3: &mut String = &mut s;
}
```