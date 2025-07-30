## HashMap<K, V>
- key-value pair

#### All keys and values must have the same type

---
### Create a HashMap 
```Rust
use std::collections::HashMap

fn main(){
	let mut scores = HashMap::new();
	// datatypes are inferred in first implementation
	scores.insert(String::from("Pancakes"), 10);
}
```

---

# Accessing data
#### get()
- Key as parameter
- returns a Option<&V>
- Option of a pointer to the value 
- No key match => None

#### contains_key()
- returns a boolean
- weather the key is registered in the map 

---

## Updating data
- HashMap must be mutable 
- inserting key multiple times only updates the value

```Rust
{
	let mut scores = HashMap::new();
	scores.insert(String::from("Alice"), 1.3);
	scores.insert(String::from("Alice"), 1.7);
	// the score will be 1.7
	println!("{:?}", scores);
}
```

---
### entry()
- insert a value if the **key does not exist** and **modify the value** (*.or_insert()*) if the key already exists
- if the key exists and you want to modify it (*.and_modify()*)
```Rust
let mut scores = HashMap::new();
scores.insert(String::from("Trufa"), 4);

// using entry to modify the value
// If the key "Trufa" did not exist, it would be created with the value 7
scores.entry("Trufa").or_insert(7);
```


### Updating value based on the old value
```ruSt
   use std::collections::HashMap;

    let text = "hello world wonderful world";

    let mut map = HashMap::new();

    for word in text.split_whitespace() {
        let count = map.entry(word).or_insert(0);
        *count += 1;
    }

    println!("{:?}", map);
```
