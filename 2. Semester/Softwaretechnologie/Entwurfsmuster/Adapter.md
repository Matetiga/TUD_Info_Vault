### Allows objects with incompatible interfaces to work together
(like a bridge to connect two different interfaces so that they can collaborate)

## Components
#### 1. Target Interface: 
- Interface to work with
#### 2. Adaptee: 
- existing class that needs to be adapted

#### 3. Adapter:
- implements the target interface and translates the client's calls into calls to the adaptee


---
#### Is a java class that implements an interface with only an empty implementation

### Motivation
=> a subclass of a interface must implement ALL the defined methods in it. 
=> An <span style="color:#ffff00">adapter of the class</span> is created in order, to <span style="color:#ffff00">implement only the needed methods</span> AND NOT every single method of the interface

---
##  Implementation
### 1. Step: Interface
```Java
interface Intref{ 
    public void m1();    
    public void m2();    
    public void m3();    
    :    
    :    
    :    
    :    
    public void m1000(); 
}
```

### 2. Step: abstract class
```java
abstract class Adapter implements Intref{ 
    public void m1(){};   
    public void m2(){};   
    public void m3(){};   
    :    
    :    
    :    
    :    
    public void m1000(){};
}
```

### 3. Step: Implementation
```java
// only the first and 80th method are needed/implemented
class Test extends Adapter{ 
    public void m1(){     
         System.out.println("This is m1() method.");    
    }        
    public void m80{     
         System.out.println("This is m80() method.");    
    } 
}
```