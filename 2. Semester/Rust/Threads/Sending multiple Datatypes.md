## With the help of [[2. Semester/Rust/Enums/Enums|Enums]]

```Rust
use std::{sync::mpsc, thread};

fn main() {
    let (tx, rx) = mpsc::channel::<Message>();
    
    thread::spawn(move || {
        let s = String::from("Hello world");
        tx.send(Message::Text(s.clone())).unwrap();
        tx.send(Message::Length(s.len())).unwrap();
    });

    for received in rx {
        match received {
            Message::Text(s) => println!("Received text: {}", s),
            Message::Length(n) => println!("Received length: {}", n),
        }
    }
}

```