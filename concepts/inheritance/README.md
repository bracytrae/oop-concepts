# Inheritance

**Inheritance** lets one class reuse and extend another class.

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

Because `Dog extends Animal`, a `Dog` can call both `eat()` and `bark()`.

Inheritance describes an **is-a** relationship: a dog is an animal. Do not use inheritance only to avoid copying code; use it when the relationship is genuinely clear.

[Back to the main guide](../../README.md)
