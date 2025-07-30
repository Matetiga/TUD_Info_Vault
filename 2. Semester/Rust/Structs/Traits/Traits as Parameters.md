Functions that implement Traits as parameters can use the types that have implemented that trait
- [[impl Trait]]
## Example
- `fn function_name(variable_name: &impl Trait_name)`

```Rust
```Rust
pub trait Summary {
	// this method does not have an implementation
    fn summarize(&self) -> String;
}


pub struct NewsArticle {
    pub headline: String,
    pub location: String,
    pub author: String,
    pub content: String,
}

impl Summary for NewsArticle {
    fn summarize(&self) -> String {
        format!("{}, by {} ({})", self.headline, self.author, self.location)
    }
}

pub struct Tweet {
    pub username: String,
    pub content: String,
    pub reply: bool,
    pub retweet: bool,
}

impl Summary for Tweet {
    fn summarize(&self) -> String {
        format!("{}: {}", self.username, self.content)
    }
}

// ---------------------------IMPORTANT-------------------------------
// Using the trait Summary as Parameter
// borrows the variable
pub fn notify(item: &impl Summary) {
    println!("Breaking news! {}", item.summarize());
}
```

## Better syntax
- this is better if we want to use as parameters more variables that are implement the same trait
```Rust
pub fn notify<T: Summary>(item: &T) {
    println!("Breaking news! {}", item.summarize());
}
```
#### Example with more variables
```Rust
pub fn notify<T: Summary>(item1: &T, item2: &T) {
```

---

## implementing structs with more Traits (as parameters)
- with the `+` Operator
- Meaning: T must implement the trait *Summary* **and** *Display*
```Rust
pub fn notify<T: Summary + Display>(item: &T) {
```

## [[Where - clause]]
- used for readability while implementing more parameters with multiple traits