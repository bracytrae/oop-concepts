# 00 — Introduction to OOP

Object-oriented programming organizes code around **objects**. An object keeps related data and actions together.

```java
class Student {
    String name; // state

    void introduce() { // behavior
        System.out.println("Hi, I am " + name);
    }
}

public class Main {
    public static void main(String[] args) {
        Student student = new Student();
        student.name = "Alex";
        student.introduce();
    }
}
```

What is happening?

1. `Student` is a **class**—a blueprint.
2. `student` is an **object** created from that class.
3. `name` is a **field** that stores state.
4. `introduce()` is a **method** that defines behavior.
5. `new Student()` creates a new instance in memory.

Next: [Encapsulation](../01-encapsulation/README.md) | [Home](../README.md)
