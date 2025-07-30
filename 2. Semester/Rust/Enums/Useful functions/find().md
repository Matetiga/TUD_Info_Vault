The method *iter()* has *find()* incorporated

#### Is used to find a specific relationship (boolean) in something iterable
### find(&mut *variable*   predicate : P)
- the predicate is a inline anonymous function, that returns [[Option<>]]
- returns first elements that satisfies the closure

```Rust
fn main() {
    let numbers = vec![1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

    // Find the first element greater than 5
    let result = numbers.iter().find(|&&x| x > 5);

    match result {
        Some(&number) => println!("Found a number greater than 5: {}", number),
        None => println!("No number greater than 5 was found"),
    }
}

```