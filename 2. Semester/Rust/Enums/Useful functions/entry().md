Is a function in order to interact with the keys of a map
- it Returns a value of the *Entry enum*:
	- **Occupied** => Key already exists in the map
	- **Vacant** => key does not exist


## or_insert()
- if the key **does not exist** in the map, it inserts it with a value
```Rust
// if the key nota is not in the map, it iserts it alongside the value 10
map.entry("Nota").or_insert(10);
```

## and_modify()
- if the **key exists,** modify it
```Rust
// it is importat to dereference num
// the closure passes a reference to the value
map.entry("Nota").and_modify(|num| *num += 5);
```