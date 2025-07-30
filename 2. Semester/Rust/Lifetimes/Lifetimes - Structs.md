
## References in structs always need a Lifetime parameter
### Example
- `<'a>` makes the Instance of *ImportantExcerpt* **i** <span style="color:#ffffff">can not outlive the reference inside the struct 
</span>

```Rust
struct ImportantExcerpt<'a> {
    part: &'a str,
}

fn main() {
    let novel = String::from("Call me Ishmael. Some years ago...");
    let first_sentence = novel.split('.').next().expect("Could not find a '.'");
    let i = ImportantExcerpt {
        part: first_sentence,
    };
}
```

