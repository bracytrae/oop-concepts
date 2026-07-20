# Classes and Objects

A **class** is a blueprint. An **object** is a value created from that blueprint.

```java
class Dog {
    String name;

    void bark() {
        System.out.println(name + " says woof!");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog(); // Create an object
        dog.name = "Milo";   // Give it state
        dog.bark();          // Ask it to perform behavior
    }
}
```

Here, `Dog` defines what every dog object can store and do. `dog` refers to one specific `Dog` object.

Each object gets its own state, so two dogs can have different names while sharing the same `bark()` behavior.

[Back to the main guide](../../README.md)
