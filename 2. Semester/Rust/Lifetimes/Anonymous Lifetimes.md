

## used when a struct implements a variable with a lifetime 
### but the compiler can infer the lifetime 


- that means the impl-Block of that struct has to implement also that lifetime parameter
- IF the **method** inside the impl-Block does **not require a specific Lifetime**, then use a <span style="color:#ffff00">anonymous Lifetime</span>

```Rust
struct MyStruct<'a> {
    name: &'a str,
    age: u8,
}

impl<'a> MyStruct<'a> {
    fn change_name(&'a mut self, new_name: &'a str) -> (&'a mut MyStruct, &'a str) {
        let old_name: &str = self.name;
        self.name = new_name;
        (self, old_name)
    }

// Anonymous lifetime 
// rust compiler infers the lifetime, because there is only one possibility 
// if : impl MyStruct => (without the lifetime) => rust compiler would throw an error, because the MyStruct definition, declares a lifetime
impl MyStruct<'_> {
    fn print_name(&self) {
        println!("My name is {:?}", self.name);
    }
}

```