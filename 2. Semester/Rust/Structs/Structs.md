[[Printing structs]]
[[Associated functions]]

---
## References in structs need always to specify [[Lifetimes - Structs]] parameters
---

#### Structs are allowed to have multiple impl blocks

###### looks like a Tuple. Like using JSON format


```Rust
struct Student{
	id: u32,
	name: String,
	graduated: bool
}

fn main(){
	let student1 = Student{
		id: 1234,
		name: String::from("martin"),
		graduated: false,
	};

	let student2 = Student{
	id: 245;
	// .. moves the remaining data of student1
	// this means that student1 cannot later be used
	..student1
	}


	// to get the a struct value: use the dot . followed by the struct value
	println("{}", student1.name)
}

```

---

### Other way to write a struct like a function
 
- The following code is a <span style="color:#ffff00">constructor</span> 
- it initializes <span style="color:#ffff00">new instances</span> of a struct 
- key:value can be omitted if <span style="color:#ffff00">parameters names match field names</span> 
```Rust
fn create_student(id: u32, name: String, graduated: bool)-> Student{

	Student{
		id, 
		name, 
		graduated
	}
}


```