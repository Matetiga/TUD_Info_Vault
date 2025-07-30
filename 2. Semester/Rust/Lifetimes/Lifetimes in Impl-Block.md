- everything should have the same lifetime

#### Lifetimes inside of the Impl-Block <span style="color:#ffff00">can be ommited</span>
- the lifetime parameter of *impl* has to match the one after *MyStruct*

```Rust
impl<'a> MyStruct<'a> {
	fn change_name(&mut self, new_name: &'a str) -> (&'a mut MyStruct, &str) {
		let old_name: &str = self.name;
		self.name = new_name;
		return (self, old_name);		
	}
}
```