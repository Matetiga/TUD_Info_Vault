## Difference with object adapter
- Class adapter Uses: <span style="color:#ffff00">Inheritance</span>
- cannot adapt `final` classes
- Object adapter uses: <span style="color:#ffff00">Composition</span> [[2. Composite]]
---
![[Screenshot from 2024-06-11 23-27-46.png]]

---
## Example:
```Java
// Class for Rectangle
public class Rectangle {
    private double width;
    private double height;

    public Rectangle(double width, double height) {
        this.width = width;
        this.height = height;
    }

    public double getArea() {
        return width * height;
    }
}

// Class for Circle
public class Circle {
    private double radius;

    public Circle(double radius) {
        this.radius = radius;
    }

    public double getArea() {
        return Math.PI * radius * radius;
    }
}

```
### the target interface
```Java
public interface Shape {
    double getArea();
}

```
### Class adapter implementation using inheritance
```Java
public class RectangleAdapter extends Rectangle implements Shape {
    public RectangleAdapter(double width, double height) {
        super(width, height);
    }

    @Override
    public double getArea() {
        return super.getArea();
    }
}

```

```Java
public class CircleAdapter extends Circle implements Shape {
    public CircleAdapter(double radius) {
        super(radius);
    }

    @Override
    public double getArea() {
        return super.getArea();
    }
}

```
### using the class adapter
```java
public class Main {
    public static void main(String[] args) {
        Shape rectangleShape = new RectangleAdapter(5, 10);
        Shape circleShape = new CircleAdapter(7);

        System.out.println("Rectangle area: " + rectangleShape.getArea());
        System.out.println("Circle area: " + circleShape.getArea());
    }
}

```