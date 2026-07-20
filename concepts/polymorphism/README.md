# Polymorphism

**Polymorphism** means the same method call can produce different behavior depending on the object.

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

A method can work with the shared `Animal` type:

```java
static void makeItSpeak(Animal animal) {
    animal.speak();
}
```

Passing a `Dog` prints `Woof!`; passing a `Cat` prints `Meow!`. `@Override` tells Java that a subclass is replacing inherited behavior.

[Back to the main guide](../../README.md)
