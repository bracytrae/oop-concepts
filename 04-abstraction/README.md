# 04 — Abstraction

**Abstraction** means showing what an object can do without making other code worry about every detail inside it.

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

`Shape` is an **interface**. It lists a method named `area()` but does not calculate the area itself. Any class that implements `Shape` promises to add its own `area()` method. This promise is sometimes called a **contract**.

`Circle` keeps that promise by providing the calculation. Code using a `Shape` only needs to call `area()`; it does not need to know which formula is used.

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
| Different classes need to provide the same methods | Related classes share data or completed methods |
| A class needs to follow more than one set of rules | A class needs one shared parent |
| You mainly want to describe what a class can do | You want to share code and require certain methods |

A Java class can implement multiple interfaces, but it can extend only one class. Neither option is always better—choose the one that makes the relationship clearest.

Previous: [Polymorphism](../03-polymorphism/README.md) | Next: [Composition](../05-composition/README.md) | [Home](../README.md)
