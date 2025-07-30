Traits that depend on other parent-traits (**Supertraits**)
- *parent traits must also be implemented*


```Rust
trait Animal{
...
}

// fly is a subtrait of Animal
trait Fly: Animal{
...
}
```