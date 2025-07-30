## Difference with class adapter
- object adapter uses: <span style="color:#ffff00">Composition</span> [[2. Composite]]
- can adapt `final` classes
- class adapter uses: <span style="color:#ffff00">Inheritance</span> 


#### adapts one interface to another using composition
=> and implements the target interface

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
### Target interface
```Java
public interface Shape {
    double getArea();
}

```
### Object adapter implementation using composition
```Java
// this class uses the instancne rectangle from class Rectngle
public class RectangleAdapter implements Shape {
    private Rectangle rectangle;

    public RectangleAdapter(Rectangle rectangle) {
        this.rectangle = rectangle;
    }

    @Override
    public double getArea() {
        return rectangle.getArea();
    }
}

```

```Java
// this class uses an circle instance from class Circle
public class CircleAdapter implements Shape {
    private Circle circle;

    public CircleAdapter(Circle circle) {
        this.circle = circle;
    }

    @Override
    public double getArea() {
        return circle.getArea();
    }
}

```

### using the object adapter
```Java
public class Main {
    public static void main(String[] args) {
        Rectangle rectangle = new Rectangle(5, 10);
        Circle circle = new Circle(7);

        Shape rectangleShape = new RectangleAdapter(rectangle);
        Shape circleShape = new CircleAdapter(circle);

        System.out.println("Rectangle area: " + rectangleShape.getArea());
        System.out.println("Circle area: " + circleShape.getArea());
    }
}

```