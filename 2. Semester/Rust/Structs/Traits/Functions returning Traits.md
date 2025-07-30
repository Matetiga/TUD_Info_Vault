- Example uses code from [[Traits]]
- because *Tweet* implements the *trait Summary* it can be returned by the function 
##### There can only be one return Type 
- adding a if clause that could alternate **with Newspaper, would not compile**


```Rust
fn returns_summarizable() -> impl Summary {
    Tweet {
        username: String::from("horse_ebooks"),
        content: String::from(
            "of course, as you probably already know, people",
        ),
        reply: false,
        retweet: false,
    }
}
```