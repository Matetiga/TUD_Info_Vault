(let us Reuse a variable name, rather than creating a new one.)
#### often use to convert a variable type to <span style="color:#ffffff">another</span>

```Rust
let spaces = "   ";
let spaces = spaces.len();

```
---


```Rust
let mut guess = String::new();

let guess: u32 = guess.trim().parse().expect("Enter a number");

 match guess.cmp(&secret_number) {
        Ordering::Less => println!("Too small!"),
        Ordering::Greater => println!("Too big!"),
        Ordering::Equal => println!("You win!"),
    }

```

*let guess: u32* and the *comparison* with secret_numbers infers that the variable *secret_number* will also be *u32* 
## -> That is why it is able to be compared
---

#### trim()
is used to erase any <span style="color:#ffffff">whitespace</span> 

#### parse()
converts String to any other type


```Rust
fn main() {
    let x = 5;

    let x = x + 1;

    {
	    // x is here: 12
	    // but this only affects within the inner scope
        let x = x * 2;
        println!("The value of x in the inner scope is: {x}");
    }
	// x is still 6
	// when we exit the previous scope, the x value returns to being 6
    println!("The value of x is: {x}");
}
```
```bash
The value of x in the inner scope is: 12
The value of x is: 6
```

