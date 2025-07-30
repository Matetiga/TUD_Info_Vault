Is a simplified match
- <span style="color:#ffff00">it is helpful when you want to match a specific variant</span> and don't want to write a complete match statement
#### Is useful (over match) when only one condition is necessary

```Rust
{
if let 0..=12 = hour {
	println!("ante meridiem");
} else if let 13..=24 = hour {
	println!("post meridiem");
} else { ... }
}
```


```Rust
fn main() {
    let some_number = Some(5);

    // Using if let to extract the value if it is Some
    if let Some(value) = some_number {
        println!("The number is: {}", value);
    } else {
        println!("No number found.");
    }
}

```