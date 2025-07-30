[[If let]]
important function to compare two variables

```Rust
match guess.cmp(&secret_numbre){
	Ordering::Less => println!("Too small"),
	Ordering::Greater => println!("Too big"),
	Ordering::Equal => println!("you win!),
	_ => // this is to catch every posible scenario
}
```

This compares *guess* and *secret_number*
 (It works like a switch function in C)

It testes the *first option (arm)*, if it does not match -> go to the next *arm*


## ref
- Keyword used in order to create references to the matched value 
- This does not take ownership of the value we want to compare 
```Rust
struct Point {
    x: i32,
    y: i32,
}

fn main() {
    let y: Option<Point> = Some(Point { x: 100, y: 200 });

    match y {
        Some(ref p) => println!("Co-ordinates are {},{} ", p.x, p.y),
        _ => panic!("no match!"),
    }
    y; // Can be used, because ownership has no been removed
}

```