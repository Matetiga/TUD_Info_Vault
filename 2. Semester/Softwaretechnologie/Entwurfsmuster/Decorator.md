#### Used to extend an objects capabilities in a flexible and reusable way
- <span style="color:#ffff00">Wraps an object with another object </span>that adds new behavior 
- This can be done multiple times, adding combinations of different behaviors

## is a restricted Composite
- with a 1-aggregation to the supperclass

![[Screenshot from 2024-05-27 11-27-24.png]]

### Components
###### 1. Component Intrerface:
- interface for original object and the decorators
- defines methods that can be implemnted
###### 2. Concrete Component:
- original object that will be decorated
###### 3. Decorator Class:
- class that implements the component interface and has a reference to a component object 

###### 4. Concrete decorators
- extend the Decorator Class and adds specific behaviors

