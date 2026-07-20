# Encapsulation

**Encapsulation** means keeping an object's data protected and controlling how other code uses it.

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

The `private` field cannot be changed directly from outside `BankAccount`. The `deposit()` method protects the object from invalid deposits.

This helps each class enforce its own rules and prevents accidental changes.

[Back to the main guide](../../README.md)
