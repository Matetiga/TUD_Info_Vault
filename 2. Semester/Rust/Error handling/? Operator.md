Because of the `?` Operator, the function will `return` an Error:
- if     `let mut username_file = File::open("hello.txt")?;` is an Error
- if     `username_file.read_to_string(&mut username)?; `is an Error
<span style="color:#ffff00">This will cause the remaining of the code not to be read</span>
- would work as if the `return` keyword would be used
	- returning the `Result<Error>`

Otherwise the function will return **Ok(username)**

```Rust
use std::fs::File;
use std::io::{self, Read};

fn read_username_from_file() -> Result<String, io::Error> {
    let mut username_file = File::open("hello.txt")?;

	// this part will not be readed if username_file throws an 
    let mut username = String::new();
    username_file.read_to_string(&mut username)?;

	println!("Hola buenas");
    Ok(username)
}

```

`?` Operator works the same as a [[Match]] clause 
- if the value is **Ok(T)** => *T* will be propagated to the rest of the code
- if the value is **Err(e)** => the error will be propagated to the rest of the function
\
---
## ? Operator is only allowed to be used in functions that return `Result<T, Err>` or `Option<T>`
- the `?` Operator *must return the same type it has worked* on 
	- if `?` was used for `Result<>` => function **must return `**Result<>` 
	- if `?` was used for `Option<>` => function **must return** `Option<>`

### `?` with: Option<>
- if return value is Some(T) => *T* is returned
- otherwise *None* is returned
```Rust
fn last_char_of_first_line(text: &str) -> Option<char> {
    text.lines().next()?.chars().last()
}
```

---

#### Using `?` in main
- Making main return `Result<T, Err>`

```Rust
use std::error::Error;
use std::fs::File;

fn main() -> Result<(), Box<dyn Error>> {
// Box<dyn Error>  means: “any kind of error.”
    let greeting_file = File::open("hello.txt")?;

    Ok(())
}
```