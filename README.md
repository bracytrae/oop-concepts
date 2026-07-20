# Object-Oriented Programming (OOP) with Java

This repository is a beginner-friendly guide to **object-oriented programming (OOP)** using Java.

OOP is a way of organizing programs around **objects**. An object groups:

- **State** — the data it stores
- **Behavior** — the actions it can perform

For example, a `Car` object might store its `color` and `speed`, and provide methods such as `accelerate()` and `brake()`.

## A small Java example

```java
class Car {
    private String color;

    Car(String color) {
        this.color = color;
    }

    void describe() {
        System.out.println("This car is " + color + ".");
    }
}

public class Main {
    public static void main(String[] args) {
        Car myCar = new Car("blue");
        myCar.describe();
    }
}
```

What is happening?

1. `Car` is a **class**: a blueprint for car objects.
2. `color` is a **field**: data stored by each car.
3. `Car(String color)` is a **constructor**: it sets up a new object.
4. `describe()` is a **method**: behavior the object provides.
5. `new Car("blue")` creates an **object** (also called an instance).

## Learning path

Read the guides in this order:

1. [Introduction to OOP](00-introduction/README.md)
2. [Encapsulation](01-encapsulation/README.md)
3. [Inheritance](02-inheritance/README.md)
4. [Polymorphism](03-polymorphism/README.md)
5. [Abstraction](04-abstraction/README.md)
6. [Composition](05-composition/README.md)

## Why use OOP?

OOP can make larger programs easier to understand by keeping related data and behavior together. It can also help you reuse code and change one part of a program without rewriting everything.

OOP is a tool, not a rule: use it when objects make the problem clearer.

## Running Java examples

Save an example in a file whose name matches its `public class`, then run:

```bash
javac Main.java
java Main
```

You need a Java Development Kit (JDK) installed. Java 17 or newer is a good choice for learning.
