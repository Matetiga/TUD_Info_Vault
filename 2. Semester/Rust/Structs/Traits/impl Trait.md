### impl Trait : 
- compiler knows exactly the type at compile time (generates code for that type)
- used for <span style="color:#00ff04">static dispatch</span>
- a way to specify the return type of a function that implements a specific trait
- **no heap allocation needed**
- [[Returning traits]]
```Rust
pub trait Area {
    fn calc_area(&self) -> f32;
}

pub fn create_shape() -> impl Area {
    Triangle { basis: 10, height: 5 }
}

```

### dyn Trait :
- the method to be called is determined at runtime 
- allows for more flexibility while using Interfaces
- <span style="color:#00ff04">dynamic dispatch</span>
- *often requires heap allocation* (with smart pointers)

## Example
```Rust
pub trait Area {
    fn calc_area(&self) -> f32;
}

pub struct Triangle {
    basis: u16,
    height: u16,
}

pub struct Circle {
    radius: u16,
}

impl Area for Triangle {
    fn calc_area(&self) -> f32 {
        (self.basis as f32 * self.height as f32) / 2.0
    }
}

impl Area for Circle {
    fn calc_area(&self) -> f32 {
        (self.radius as f32).powi(2) * 3.14
    }
}

// Function that accepts any type implementing the Area trait
// the parameter in this function can also be:
// => form: &dyn Area
// => form: Box(dyn Area)
pub fn print_area(form: impl Area) {
    println!("The area is: {}", form.calc_area());
}

```

---
### Difference with `impl Trait`
```Rust
pub struct Screen<T: Draw> {
    pub components: Vec<T>,
}

impl<T> Screen<T>
where
    T: Draw,
{
    pub fn run(&self) {
        for component in self.components.iter() {
            component.draw();
        }
    }
}
```

This restricts us to a `Screen` instance that has a list of components all of type `Button` or all of type `TextField`. If you’ll only ever have homogeneous collections, using generics and trait bounds is preferable because the definitions will be monomorphized at compile time to use the concrete types.