- this is then used to retrieve the value of Option<>
- not the *None*

```Rust
fn find_even_number(numbers: &[i32]) -> Option<i32> {
    for &num in numbers {
        if num % 2 == 0 {
            return Some(num);  // returns the first even number found
        }
    }
    None  // returns None if no even numbers are found
}

fn main() {
    let numbers = vec![1, 3, 5, 7, 10, 11];
    match find_even_number(&numbers) {
	    // this retrieves the interger retuned by the function 
	    // and stores it in the variable "even"
        Some(even) => println!("The first even number is: {}", even),
        None => println!("No even numbers found."),
    }
}

```
