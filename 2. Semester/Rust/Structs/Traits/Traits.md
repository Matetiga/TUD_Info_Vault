[[Traits as Parameters]]
	 [[impl Trait]]
## Not Specified Traits - specified impl
- *can* work like interfaces in Java
- each [[2. Semester/Rust/Structs/Structs|Structs]] that wants the trait must **implement it by themselves**
- 

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
// implementation of Summary by NewsArticle
impl Summary for NewsArticle {
    fn summarize(&self) -> String {
        format!("{}, by {} ({})", self.headline, self.author, self.location)
    }
}
// implementation of Summary by Tweet
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
```


## Specified Traits - Not Specified implementation
###### a Specified trait method can be <span style="color:#ffffff">overridden</span> if there is an implementation of it 

- have an implementation of the method
- this method will be passed to all structs that use this trait (**no modification possible**)
- then => `impl Summary for NewsArticle` <span style="color:#ffffff">must be empty</span>
 
```Rust
trait Summary{
	fn summarize(&self)->String{
		String::from("read more...")
	}
}
  
#[allow(dead_code)]
struct NewsArticle{
	headline: String,
	location: String,
	author: String,
	content: String,
}
  
impl Summary for NewsArticle{}
  
fn main() {
	let article = NewsArticle {
	headline: String::from("Penguins win the Stanley Cup Championship!"),
	location: String::from("Pittsburgh, PA, USA"),
	author: String::from("Iceburgh"),
	content: String::from(
	"The Pittsburgh Penguins once again are the best \
	hockey team in the NHL.",
		),
	};
  
	println!("New article available! {}", article.summarize());
}
```