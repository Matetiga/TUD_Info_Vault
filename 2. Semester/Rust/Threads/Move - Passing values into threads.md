- *move* keyword inside the closure
	- <span style="color:#ffff00">only the variables that are declared outside the thread, are taken ownership from inside the thread closure</span>
	- makes the thread **take ownership of v**
- variable from main thread is used in thread:spawn

```Rust
use std::thread;

fn main() {
    let v = vec![1, 2, 3];

    let handle = thread::spawn(move || {
        println!("Here's a vector: {v:?}");
    });

    handle.join().unwrap();
}
```