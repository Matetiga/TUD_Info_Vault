## Differences with [[2. Semester/Rust/Structs/Structs|Structs]]
- Enums are used to define a type that can be of different variants
- are helpful to encapsulate multiple datatypes inside of one
	- [[Sending multiple Datatypes]]

```Rust
enum Message {
    Quit,
    Move { x: i32, y: i32 },
    Write(String),
    ChangeColor(i32, i32, i32),
}
```

---

```Rust
enum my_enum{
	variable_1(String);
	variable_2(String);
	
}

fn main(){
	let x = my_enum::variable_1(String::from("buenas"));
	let y = my_enum::variable_2(String::from("tardes"));
}
```


### If the None part is not used
```rust
    let config_max = Some(3u8);
    if let Some(max) = config_max {
        println!("The maximum is configured to be {}", max);
    } else { // else bloc would be the same as _ below
	    config_max += 1;
    }
```
#### This is the same as
```Rust
    let config_max = Some(3u8);
    match config_max {
        Some(max) => println!("The maximum is configured to be {}", max),
        // _ is used for all other ocasions 
        _ => (),
    }

```