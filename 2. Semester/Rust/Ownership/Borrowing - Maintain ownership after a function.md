[[Borrowing rules]]
## [[2. Semester/Rust/Ownership/References]] are inmutable by default

#### This is made by "borrowing" a variable 
=> with a pointer (Reference)

```Rust 
fn main(){
	let a = String::from("hola tonotos");
	still_owner(&a);
	
	println!("this will compile, {a}");
}

fn still_owner(input: &String){
	pritnln!("Content of the string is: {input}");
	
}
```

#### We create a pointer &String, that points to a, which points to the heap 
![[WhatsApp Image 2024-04-25 at 20.05.22.jpeg]]

# [[Borrowing rules]]
