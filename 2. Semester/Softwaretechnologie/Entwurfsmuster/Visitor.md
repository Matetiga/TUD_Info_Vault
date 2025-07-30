Involves separating an algorithms firm the object on which it operates
##### Useful for complex object structures and you want to perform operation of these objects without changing their classes

## Components
### 1. Visitor Interface:
- defines a visit method for each type of element that can be visited
### 2. Concrete Visitor:
- implements Visitor Interface and defines operations to be performed on its elements

### 3. Element Interface:
declares an `accept` method that takes **visitors as arguments**

### 4. Concrete Elements:
- implement the Element Interface and the `accept` method, which call the visitor's visit method

