Just like a fabric creates a car based on specifications
[[Biologisches Programmieren]]

- ## [[Instances]] 
- ## [[Constructor]]
- ## [[Methods]]

```Java
public class Human(){

	//Instances (like global variables)
	private String name;
	private String last_name;

	// The constructor has the same name as the class
	public Human(String name, String last_name){

	//this.name refers to the instance!! (thanks to this.)
	this.name = name;
	this.last_name = last_name;
	}

	// Method returns a String value
	public String getName(){
		return name;
	}
}
```
---
## [[Vererbung]]
Subclasses inherit characteristics of Superclasses

## Redefinition
if a method is <span style="color:#ffff00">called again</span> in a Subclass, then it is redefined
This <span style="color:#ffff00">hides the method</span> (characteristic) of the <span style="color:#ffff00">Superclass</span>

=> <mark style="background: #FFB86CA6;">Reason</mark>: the search algorithm, searches bottom-up 
