- Used for a clearer Syntax, which variable implements which Trait(s)
---
[[impl Trait]]
## Example
- *T* implements the Traits `Display` and `Clone`
- *U* implements the Traits `Clone` and `Debug`

```Rust
fn some_function<T, U>(t: &T, u: &U) -> i32
where
    T: Display + Clone,
    U: Clone + Debug,
{

```
### instead of 
```Rust
fn some_function<T: Display + Clone, U: Clone + Debug>(t: &T, u: &U) -> i32 {
```