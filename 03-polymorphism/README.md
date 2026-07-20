# 03 — Polymorphism

**Polymorphism** lets the same method call behave differently for different objects.

```java
class Animal {
    void speak() {
        System.out.println("Animal sound");
    }
}

class Dog extends Animal {
    @Override
    void speak() {
        System.out.println("Woof!");
    }
}

class Cat extends Animal {
    @Override
    void speak() {
        System.out.println("Meow!");
    }
}
```

Calling `speak()` on a `Dog` prints `Woof!`; calling it on a `Cat` prints `Meow!`. The `@Override` annotation confirms that each child class replaces inherited behavior.

This allows one piece of code to work with many related object types.

Previous: [Inheritance](../02-inheritance/README.md) | Next: [Abstraction](../04-abstraction/README.md) | [Home](../README.md)
