#### Can NOT be mutable 
#### All uppercase (with underscores as spaces)
---

- Their Data Type must always be assigned
- They must be <span style="color:#ffff00">set to a constant expression</span> 


```Rust
const THREE_HOURS_IN_SECONDS: u32 = 60 * 60 * 3;
// 3 i the number of hours we want to count with the program
```

## Constants can be used as global variables
whereas <span style="color:#ffff00">let</span> can only be used inside of functions