---
command:
---


(also used to keep the code organized)

The <span style="color:#ffff00">Cargo.toml </span>keeps the relevant dependencies of the code (libraries...)

---
##### command:: cargo new
new cargo proyect

---
in **/src** remains the important code 
in **/target** lays the executable files (after compiling)
*cargo build* compiles the file 
run it with: *./target/debug/file_name* 
##### command:: cargo run 
compiles and runs the program

##### command:: cargo check
checks if the code is able to compile (**but it does not run it**)

##### command:: cargo build --release
to compile with optimizations (it will create */target/release*)

---
<span style="color:#ffff00">Cargo.lock</span> keeps track of the versions of the dependencies

