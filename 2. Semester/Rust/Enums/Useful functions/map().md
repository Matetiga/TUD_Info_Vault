## Used to changed the values inside *Option* and *Result* applying a function 

```Rust
fn main() {
    let some_number = Some(5);
    let incremented_number = some_number.map(|x| x + 1);
    println!("{:?}", incremented_number); // Output: Some(6)

    let no_number: Option<i32> = None;
    let still_no_number = no_number.map(|x| x + 1);
    println!("{:?}", still_no_number); // Output: None
}

```