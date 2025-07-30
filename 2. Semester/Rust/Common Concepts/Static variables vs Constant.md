## Static variables
- have a fixed address in the memory
- can be **mutable**
- defined in the global scope

## Constant variable
- implement the *Copy trait*
- are always **immutable** 
- defined in the global scope

```Rust
static EIGHT:u8 = 8;
const NINE:u8 = 9;
const MY_ARRAY:[i32; 5] = [1, 2, 3, 4, 5];
```