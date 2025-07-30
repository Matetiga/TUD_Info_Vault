[[Functions]]
```Rust
use std::io

let mut guess = String::new();

// using stdin function from io module
io::stdin()
	.read_line(&mut guess)
	.expect("Failed to read line");
// another way to write this part: 
//io::stdin().read_line(&mut guess).expect("Failed to read line");
```

<span style="color:#ffffff">this function returns a string </span>

If we hadn't imported std::io library -> we could <span style="color:#ffffff">still use the stdin function:</span>
=> <span style="color:#ffffff">std::io::stdin</span>
#### The <span style="color:#ffffff">::</span> syntax indicates that <span style="color:#ffffff">new</span> is a [[associated function]]

---

