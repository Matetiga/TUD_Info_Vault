Threads are dependent on the main thread. 
- if The main thread ends: other threads are terminated


Threads are used to run simultaneously various parts of the code
- the runtime order can be random (depends on the cores of the computer)
- therefore the results may vary from one run to another
## Creating a thread
- following code **will stop**, when the *main* thread `(not thread: :spawn)` *stops* running 

```Rust
use std::thread;
use std::time::Duration;

fn main() {
    thread::spawn(|| {
        for i in 1..10 {
            println!("hi number {i} from the spawned thread!");
            thread::sleep(Duration::from_millis(1));
        }
    });

    for i in 1..5 {
        println!("hi number {i} from the main thread!");
        thread::sleep(Duration::from_millis(1));
    }
}
```

---

## [[Move - Passing values into threads]]
