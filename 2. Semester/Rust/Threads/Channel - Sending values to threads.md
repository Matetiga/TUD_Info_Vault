- Let us pass information between threads
- Unidirectional
- when the receiver or sender is dropped => channel also dropped 
- <span style="color:#ffff00">Multiple producers but only one receiver</span> 


## Creating a channel
- tx => traditional name for transmitter-end
- rx => traditional name for receiver-end

- using *move* to pass *tx* into the thread
- `send` method returns *Result<T, E>*
```Rust
use std::sync::mpsc;
use std::thread;

fn main() {
    let (tx, rx) = mpsc::channel();

    thread::spawn(move || {
        let val = String::from("hi");
        tx.send(val).unwrap();
    });


    let received = rx.recv().unwrap();
    println!("Got: {}", received);

}
```

### Receiver methods:
- recv() => returns `Result<T, RecvError>`
	- this blocks the main thread execution, until the value is sent down the channel
	
- try_recv()  => returns `Result<T, TryRecvError>`
	- the main thread is not blocked

```Rust
use std::sync::mpsc;
use std::thread;
use std::time::Duration;

fn main() {
    let (tx, rx) = mpsc::channel();

    thread::spawn(move || {
        let vals = vec![
            String::from("hi"),
            String::from("from"),
            String::from("the"),
            String::from("thread"),
        ];

        for val in vals {
            tx.send(val).unwrap();
            thread::sleep(Duration::from_secs(1));
        }
    });

    for received in rx.recv() {
        println!("Got: {}", received);
    }
}
```