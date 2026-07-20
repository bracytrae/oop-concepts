# 01 — Encapsulation

**Encapsulation** protects an object's data and controls how it can be changed.

```java
class BankAccount {
    private double balance;

    void deposit(double amount) {
        if (amount > 0) {
            balance += amount;
        }
    }

    double getBalance() {
        return balance;
    }
}
```

The `private` field cannot be changed directly from outside `BankAccount`. Other code must use `deposit()`, which rejects invalid amounts. This keeps the object in a valid state.

Use encapsulation when a class needs to protect rules about its data.

Previous: [Introduction](../00-introduction/README.md) | Next: [Inheritance](../02-inheritance/README.md) | [Home](../README.md)
