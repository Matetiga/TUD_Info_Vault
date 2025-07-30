## Clone-on-write
`Cow` stands for "Clone On Write." It's a smart pointer provided by Rust that allows you to work efficiently with data that might need to be mutated or might remain unchanged. The idea is to *avoid unnecessary cloning* of data **unless it's actually required**

### Example:
- there is data that must be read
	- *occasionally* this data must be changed 
	- clone the data every time is inefficient

---

## Cow- States
### Borrowed:
- It holds an immutable reference to the data (`&T`).
	- when you **try to mutate on the borrowed state**, it will automatically clone the variable

### Owned: 
- It holds an owned version of the data (`T`)


```Rust
use std::borrow::Cow;

fn main() {
    let s = "Hello, world!".to_string();
    let cow: Cow<str> = Cow::Borrowed(&s);

    // Initially, cow is in the Borrowed state
    print_cow(&cow);

    // Convert cow to Owned state if we need to mutate it
    let mut cow = cow.into_owned();
    cow.push_str(" Nice to meet you!");

    let cow: Cow<str> = Cow::Owned(cow);
    print_cow(&cow);
}

fn print_cow(cow: &Cow<str>) {
    match cow {
        Cow::Borrowed(borrowed) => println!("Borrowed: {}", borrowed),
        Cow::Owned(owned) => println!("Owned: {}", owned),
    }
}
```