#### It is used so <span style="color:#ffffff">only one</span> thread at a time can use a specific variable
- the value can be accessed using => <span style="color:#ffff00">lock() / try_lock()</span> 
	- calling *lock()* would panic if another thread is using the same variable => therefore is *unwrap()* called
	- [[Arc<T> - Multiple Ownership inside threads]]
```Rust
use std::sync::Mutex;

fn main() {
    let m = Mutex::new(5);

    {
        let mut num = m.lock().unwrap();
        *num = 6;
    }

    println!("m = {:?}", m);
}
```


## Example
- using `Arc<T>`
```Rust
use std::sync::{Arc, Mutex};
use std::thread;

fn main() {
    let counter = Arc::new(Mutex::new(0));
    let mut handles = vec![];

    for _ in 0..10 {
        let counter = Arc::clone(&counter);
        let handle = thread::spawn(move || {
            let mut num = counter.lock().unwrap();

            *num += 1;
        });
        handles.push(handle);
    }

    for handle in handles {
        handle.join().unwrap();
    }

    println!("Result: {}", *counter.lock().unwrap());
}
```