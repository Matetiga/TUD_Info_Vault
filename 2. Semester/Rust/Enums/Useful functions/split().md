To separate a string, when a desired character pops in 

#### Can also be done with a closure
```Rust
let word_vec: Vec<&str> = contenido.split(|caracter|caracter == ' ' || caracter == '\n' ).collect();
```