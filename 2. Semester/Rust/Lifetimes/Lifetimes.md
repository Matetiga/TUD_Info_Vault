##### Specially used when using references


- when passing references and returning references, the compiler does not know **how the parameters references relate to the returned reference**


## Annotation in  Functions
### Lifetime 'a 
- this ensures every parameter has the same lifetime => `'a`
```Rust
fn longest<'a>(x: &'a str, y: &'a str) -> &'a str {
    if x.len() > y.len() {
        x
    } else {
        y
    }
}

```