
- the implementation is similar to the [[Traits as Parameters]]
	- <span style="color:#ffff00">keyword:</span> *dyn*
	- stands for dynamic (trait object allows *dynamic dispatch of methods*)
	- <span style="color:#ffff00">trait objects are a pointer to some data that implements the Trait</span>
	- often **used with smart pointers** (*Box, Rc, Arc*)

#### Is a way to work with different types that implement the same trait <span style="color:#ffff00">without knowing </span>the specific type at <span style="color:#ffff00">compile time</span>

```Rust
fn describe_anything(item: &dyn Describable)
```


---

## Differences with [[impl Trait]]
- ### dyn Trait :
- the method to be called is determined at runtime 
- allows for more flexibility while using Interfaces
- <span style="color:#00ff04">dynamic dispatch</span>

---

# Implementation
#### Trait Object definition ==`Box<dyn Trait>
- this allows for multiple types to fill the implementation at runtime
- `Vec<T>` **can hold** (e.g) `Box<Button>` **as well** as `Box<TextField>`

```Rust
pub struct Screen {
    pub components: Vec<Box<dyn Draw>>,
}

impl Screen {
    pub fn run(&self) {
        for component in self.components.iter() {
            component.draw();
        }
    }
}
```

