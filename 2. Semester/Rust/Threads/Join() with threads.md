
## Using join()
- store thread:spawn inside a variable `(handle)`
- join() => will make the main thread wait until the thread:spawn finishes
- if we move *handle.join().unwrap();* to the middle => thread:spawn will finish working and **then lets the main thread start**

```Rust
use std::thread;
use std::time::Duration;

fn main() {
    let handle = thread::spawn(|| {
        for i in 1..10 {
            println!("hi number {i} from the spawned thread!");
            thread::sleep(Duration::from_millis(1));
        }
    });

	//handle.join().unwrap();

    for i in 1..5 {
        println!("hi number {i} from the main thread!");
        thread::sleep(Duration::from_millis(1));
    }

    handle.join().unwrap();
}
```
