# 04 — Abstraction

**Abstraction** exposes what an object can do while hiding how it does it.

```java
interface Shape {
    double area();
}

class Circle implements Shape {
    private final double radius;

    Circle(double radius) {
        this.radius = radius;
    }

    public double area() {
        return Math.PI * radius * radius;
    }
}
```

`Shape` defines a promise: every shape must provide `area()`. Code using a `Shape` does not need to know the formula used by each implementation.

Java commonly uses **interfaces** and **abstract classes** to create abstractions.

Previous: [Polymorphism](../03-polymorphism/README.md) | Next: [Composition](../05-composition/README.md) | [Home](../README.md)
