Used to have just the data-types on the fields rather than names
- Used to give the whole tuple a name
- Used when the variables names inside of the tuple repeat themselves

###### A tuple struct cannot have another tuple struct as a parameter (even though their datatypes match)

```Rust
// the 
struct Color(i32, i32, i32);
struct Point(i32, i32, i32);
```