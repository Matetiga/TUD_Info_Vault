## Rules that the compiler uses to infer the lifetimes of parameters in functions

### 1. Rule
- assign a lifetime to each parameter that is a reference
```Rust
fn example_function(param1: &u8, param2: &u8)
->
fn example_function<'a, 'b>(param1: &'a u8, param2: &'b u8)
```

---

### 2. Rule
- If only one input lifetime exists after rule one, all output lifetimes are equal to the input lifetime
```Rust
fn example_function<'a>(param1: &'a u8) -> &u16
->
fn example_function<'a>(param1: &'a u8) -> &'a u16
```

---

### 3. Rule
- If multiple input lifetimes exist and one is &self or &mut self, the lifetime of self is applied to all output parameters
```Rust
fn example_method(&self, param2: &u8) -> &u8
// 1. Rule 
->
fn example_method<'a, 'b>(&'a self, param2: &'b u8) -> &u8
// 2. Rule does NOT apply -> then use 3. Rule
->
fn example_method<'a, 'b>(&'a self, param2: &'b u8) -> &'a u8
```

---
