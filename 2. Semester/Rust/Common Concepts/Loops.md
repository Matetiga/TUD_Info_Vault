### break and return work alike 
- both return a variable 
- the semicolon can be left aside
```Rust 
fn main(){
	let mut counter = 0;
	loop{
		counter += 1;
		if counter == 3{
		// the semicolon can be put or left aside
			break counter + 2
		}
	}
}
```

# loop
- works as a while loop, but without condition 
- runs for eternity (break it with : ctrlC)
```Rust
fn main(){
	let counter = 0;
	let y = loop{
		counter += 1
	}

	println!("{counter}"); // prints
}
```

### Inner loops can break outer loops!
Syntax: **'** (with a single apostrophe)
```Rust 
	fn main(){
	let mut new_counter = 0;
	
		'counting: loop{
		
			println!("the counter is {counter}");		
			let mut variable = 10;
			
			loop{
				println!("variable: {variable}");
				if variable == 9{
				// this will break only this inner loop
				break;
			}
			
			else if new_counter == 2{
				println!("breaking the first loop");			
				// this will break the whole outer loop			
				break 'counting;			
			}						  			
			variable -= 1;			
			}
		new_counter += 1;
		
		}
		
	}
}
```


# while 
```Rust
fn main(){
	let counter = 2; 
	while counter != 4{
		println!("ola");
		counter += 1;
	}
}
```
# for
- There is also an option: instead of using for-loops => use [[find()]]

useful for iterating trough arrays
Uses [[Slices]]
#### it works like python for-loops
```Rust
fn main(){
	let a = [1, 2, 3, 4, 5]

	for element in a {
		println!("printing each element from a {element}");
	}

	for number in (1..5){
		// this prints number in range 1 to 4
		println!("prints the nunmber {number}")
		
	}
}
```



