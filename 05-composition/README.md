# 05 — Composition

**Composition** builds a class from other objects. It describes a **has-a** relationship.

```java
class Engine {
    void start() {
        System.out.println("Engine started");
    }
}

class Car {
    private final Engine engine = new Engine();

    void start() {
        engine.start();
        System.out.println("Car is ready");
    }
}
```

A car **has an** engine, so `Car` delegates part of its work to an `Engine` object. Neither class needs to inherit from the other.

Composition often makes code easier to change because you can replace one component without changing the whole class hierarchy. A useful guideline is: **favor composition over inheritance** when the relationship is has-a rather than is-a.

Previous: [Abstraction](../04-abstraction/README.md) | [Home](../README.md)
