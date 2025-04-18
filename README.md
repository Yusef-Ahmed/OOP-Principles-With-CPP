# OOP Principles With CPP

Object-Oriented Programming (OOP) principles are the foundational ideas behind organizing software design around objects rather than functions or logic. 

There are four main OOP principles, often referred to as the pillars of OOP

## 1. Encapsulation

### Description

Encapsulation means hiding the internal state and requiring all interaction to be performed through an object’s methods.


#### Code

```cpp
#include <iostream>
using namespace std;

class BankAccount {
private:
    double balance;  // private data

public:
    BankAccount(double initial) {
        balance = initial;
    }

    void deposit(double amount) {
        balance += amount;
    }

    double getBalance() {
        return balance;
    }
};

int main() {
    BankAccount acc(1000);
    acc.deposit(500);
    cout << acc.getBalance();  // Output: 1500
}
```

Without it, I can do something like `acc.balance = 999` or corrupt the data
