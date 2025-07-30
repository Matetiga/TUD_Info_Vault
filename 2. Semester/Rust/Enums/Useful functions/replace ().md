- replaces the Option value with a new value 
- Returns old value
- If Option *value is None* = *Some value* with the new value replaces it 
```Rust
fn main() {
    let mut vec = vec![1, 2, 3, 4, 5];

    // Replacing the first element and capturing the old value
    let old_value = std::mem::replace(&mut vec[0], 10);

    println!("Old value: {}", old_value); // Output: Old value: 1
    println!("New vector: {:?}", vec);    // Output: New vector: [10, 2, 3, 4, 5]
}
