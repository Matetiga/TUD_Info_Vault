#### Useful when working with iterators and want to process values until you run out of them

```Rust
while let PATTERN = EXPRESSION{
...
}
```

### while let
```rust
{

let mut counter  = 0;

while let 0 | 1 | 2 | 3 = number {
	println!("Counter: {}", number);
	counter += 1;

}
```

### while 
```rust
let mut counter = 0;
while counter < 4 {
	println!("Counter: {}", counter);
	counter += 1;
}
```