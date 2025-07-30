### Rust is kinda OOP
**Objects** pack data and procedures (*can be called with methods*)

---
### However
- handles Inheritance through Traits (**Not classes** )


---

## Abstraction
- split code in several parts and allow reuse 
- is a design pattern 
- Example: **unspecified functions in Traits** <=> Abstract base class
	- *Abstract Base classes : define behavior to its subclasses*

## Encaptulation
- refers to bundling (agrupacion) of data with methods that operate on that data
- access to the state is only possible **through the object's** methods
	- <span style="color:#ffffff">Modules, Structs</span> <=> <span style="color:#ffff00">Encapsulate data</span>
	- <span style="color:#ffffff">Traits </span><=> <span style="color:#ffff00">define behavior</span>
## Polymorphism 
- permit **child classes to be used** where their **parent classes are used**

## Inheritance
- through traits