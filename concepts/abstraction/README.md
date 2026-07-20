# Abstraction

**Abstraction** shows what an object can do while hiding unnecessary implementation details.

```java
interface Shape {
    double area();
}

class Rectangle implements Shape {
    private final double width;
    private final double height;

    Rectangle(double width, double height) {
        this.width = width;
        this.height = height;
    }

    public double area() {
        return width * height;
    }
}
```

The `Shape` interface defines a simple promise: every shape provides `area()`. Code using a `Shape` does not need to know how each shape calculates its area.

Interfaces are a common Java tool for abstraction.

[Back to the main guide](../../README.md)
