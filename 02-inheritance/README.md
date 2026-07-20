# 02 — Inheritance

**Inheritance** lets a class reuse and specialize another class.

```java
class Animal {
    void eat() {
        System.out.println("Eating...");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Woof!");
    }
}
```

`Dog extends Animal` means a dog inherits `eat()` and adds `bark()`. This represents an **is-a** relationship: a dog is an animal.

Use inheritance only when the child really is a more specific version of the parent. For simply combining features, composition is often clearer.

Previous: [Encapsulation](../01-encapsulation/README.md) | Next: [Polymorphism](../03-polymorphism/README.md) | [Home](../README.md)
