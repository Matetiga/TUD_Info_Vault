# Implementation
```Rust
let mut s1 = String::new();
let mut s2 = "hola buenas".to_string();
let mut s3 = String::from("ola buenas");
```

---
# Updating a string
#### push()
- add single character to a string
#### push_str()
- add a string literal to a string

### Concatenate strings
- format! => does not affect Ownership
- +
```Rust
let s1 = String::from("ola");
let s2 = format!("tonotos {}", s1);
// first must be a String, next ones a &str
let s3 = s1+ &s2;
```

---

# Getting a character
#### char()
- chained with .collect() returns the characters in a vector

#### bytes()
- returns the corresponding binary representation 

---
## String components:
- ptr: points towards the heap **(8 Bytes)**
- len: total size of the string **(8 Bytes)**
- capacity (): space received from the system **(8 Bytes)**
	- *Total space of a String* => **24 Bytes**

```Rust 
fn main(){
	// this syntax allows the variable string to be mutable
	let my_string: String = String::form("hola");
	// this will bind both strings
	my_string.push_str(" mundo");
	

	// this is a string literal: not mutable 
	let _string "holas";
	
}
```

## Return a string 
- as a return value of a function, and not to print it
```Rust
fn a_function()->String{
	return format!("Hola tonotos")
}
```

---

# Difference &String and &str
- **&String is a reference (<span style="color:#ffffff">pointer stored in the stack</span>) to a String (<span style="color:#ffffff">content that is stored in the heap</span>)** 
	- immutable 
	- can only be used to reference a String
- &str is a **reference (located in the stack)** for a "hard-coded" <span style="color:#ffffff">content</span> **in the binary**
	- immutable
	- can be used also for string slices
