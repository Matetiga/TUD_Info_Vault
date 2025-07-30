### Creates an iterator of cloned values

```Rust
fn main() {
    let v = vec![1, 2, 3, 4, 5];

    let cloned_iter = v.iter().cloned(); // Creates an iterator of cloned values

    for val in cloned_iter {
        println!("{}", val);
    }
}

```

## Differences with clone()
- clone() is for types that implement the *Clone trait*
- 