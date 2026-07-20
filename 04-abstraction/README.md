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

## Abstract classes

An **abstract class** is a class that cannot be used to create objects directly. It can contain shared fields, completed methods, and abstract methods that subclasses must implement.

```java
abstract class Animal {
    private final String name;

    Animal(String name) {
        this.name = name;
    }

    void introduce() { // Concrete method: already implemented
        System.out.println("I am " + name);
    }

    abstract void speak(); // Abstract method: no implementation yet
}

class Dog extends Animal {
    Dog(String name) {
        super(name);
    }

    @Override
    void speak() {
        System.out.println("Woof!");
    }
}
```

You cannot write `new Animal()` because `Animal` is abstract. You can create a `Dog`, which inherits `introduce()` and supplies the missing `speak()` behavior. `super(name)` calls the parent constructor.

## Interface or abstract class?

| Use an interface when... | Use an abstract class when... |
| --- | --- |
| Unrelated classes should follow the same contract | Closely related classes share state or code |
| A class may need several contracts | A class needs one shared parent |
| You mainly want to describe capabilities | You want both a foundation and required behavior |

A Java class can implement multiple interfaces, but it can extend only one class. Neither option is always better—choose the one that makes the relationship clearest.

Previous: [Polymorphism](../03-polymorphism/README.md) | Next: [Composition](../05-composition/README.md) | [Home](../README.md)
