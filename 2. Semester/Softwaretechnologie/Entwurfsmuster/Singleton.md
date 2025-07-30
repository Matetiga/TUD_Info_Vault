### Ensures that a class has<span style="color:#ffffff"> only one instance</span> and provides a <span style="color:#ffffff">global point of access</span> to that instance

=> Useful when exactly one object is needed

## Components:
#### 1. Private Constructor:
- prevent other classes from instantiating the Singleton 
#### 2. Private Static Instance:
- Holds the single instance of the class

#### 3. Public Static Method:
- Global access to the single instance


# UML
![[Screenshot from 2024-05-29 13-38-45.png]]

## Implementation
#### 1. Step
```Java
public class SingleObject {

   //create an object of SingleObject
   private static SingleObject instance = new SingleObject();

   //make the constructor private so that this class cannot be
   //instantiated
   private SingleObject(){}

   //Get the only object available
   public static SingleObject getInstance(){
      return instance;
   }

   public void showMessage(){
      System.out.println("Hello World!");
   }
}
```

#### 2. Step
```Java
public class SingletonPatternDemo {
   public static void main(String[] args) {

      //illegal construct
      //Compile Time Error: The constructor SingleObject() is not visible
      //SingleObject object = new SingleObject();

      //Get the only object available
      SingleObject object = SingleObject.getInstance();

      //show the message
      object.showMessage();
   }
}
```