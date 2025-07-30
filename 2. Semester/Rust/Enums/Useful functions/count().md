Counts the number of elements inside an iterator

```Rust
fn main() {
	let vec: Vec<u16> = (1..=10).collect();

	println!("the amount of elements is {}", vec.iter().count());
}
```