```Rust
struct Student{
	name: String,
	age: u8,
}


impl creating_student(this_name: String, this_age: u8)->Strudent{
	Student{
		name : this_name
		age: this_age
	}
}
```

#### When the struct variables are the same to the constructors variables 
```Rust
impl creating_student(name: String, age: u8)->Strudent{
	Student{
		name,
		age,
	}
}
```