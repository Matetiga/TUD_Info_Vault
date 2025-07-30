A generic type in programming languages like Java allows you to define classes, interfaces, or methods with placeholders for types (type parameters) that are specified later when the code is used.

For example, in Java, you can define a generic class like this:

java
```Java
public class Box<T> {
	private T content; 
	
	public void setContent(T content){
	    this.content = content; 
	}   
	public T getContent(){
	    return content;
    }
 }
```
Here, `<T>` is a type parameter that represents the type of the content stored in the `Box`. When you create an instance of `Box`, you specify the actual type to be used in place of `T`. For example: