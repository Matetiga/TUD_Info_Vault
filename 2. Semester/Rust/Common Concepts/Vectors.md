*Vectorrr, it's me*
Unlike arrays, vectors do <span style="color:#1fffc7">not have a fixed size</span> 
##### they look like a tuple, but can only hold one data-type


## Initialize a Vector
- 3 different ways to initialize a vector
```Rust
// vector with the digits 1, 2 and 3 
let mut vector_1 : Vec<i32> = Vec::new();
let mut vector_2 = Vec::<i32>::new();
let mut v: Vec<i32> = vec![1, 2, 3];
// digit 4 is being added to the vector
v.push(4);

```
###### if a new element is added to the vector, the array size is increased, which makes all previous elements to be copied in another memory location, alongside with the new element

---

### Example:
```Rust
fn main() {
	let mut v: Vec<i32> = vec![1, 2, 3];
	let num: &i32 = &v[2];
	v.push(4);
	println!("Third element is {}", *num); // this is invalid
}
```
[[2. Semester/Rust/Ownership/References]]
=> num is a pointer to the second element in the vector heap, but after the push, the whole vector is **deallocated and allocated** in another memory position. Therefore the **previous pointer is invalid**

---

# Callable methods with Vectors
#### len()
- returns number of items stored
#### capacity()
- return items storable
```Rust
// this has a capacity of 4
let mut v1 : Vec<i32> = Vec::with_capacity(4);
```

#### push()
- adds a new element to the vector
- automatic resize

#### remove()
- remove element of vector at index 
- Crashes if index does not exist
- removed item is <span style="color:#ffff00">also returned</span> 

---

# Accessing data 
##### using *vector_name*.index
---
#### get()
- with Index as a parameter
- returns an Option


---
# Iterating a vector

## For-loop
```Rust
let v1 : Vec<char> = vec!['a', 'b' , 'c'];

for character in &v1{
	print!("{}", character);
}
```

### iterate and mutate 
```Rust
let v1 : Vec<i32> = vec![1, 2, 3, 4];

for num in &mut v1{
	*num += 10;
}

```

---

# Vector with multiple datatypes
## Using Enum
```Rust
#[derive(Debug)]
enum MyVector {
	Int(i32),
	Float(f64),
	Text(String),
}


fn main() {
	let v1 = vec![
		MyVector::Int(42),
		MyVector::Text(String::from("I am a number")),
		MyVector::Float(8.15),
	];
	println!("{:#?}", v1);
}
```