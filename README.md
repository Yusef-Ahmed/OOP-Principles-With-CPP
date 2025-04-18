# OOP Principles With JS

Object-Oriented Programming (OOP) principles are the foundational ideas behind organizing software design around objects rather than functions or logic. 

There are four main OOP principles, often referred to as the pillars of OOP

## 1. Encapsulation

### Description

Encapsulation means hiding internal data and only exposing what's necessary.


### Code

```js
class BankAccount {
  #balance; // private field

  constructor(initialBalance) {
    this.#balance = initialBalance;
  }

  deposit(amount) {
    this.#balance += amount;
  }

  getBalance() {
    return this.#balance;
  }
}

const acc = new BankAccount(1000);
acc.deposit(500);
console.log(acc.getBalance()); // 1500
// console.log(acc.#balance); // Error: private field
```

## 2. Abstraction

### Description

Abstraction means hiding complex logic and only showing what’s important.

### Code

```js
class Car {
  start() {
    this.#igniteEngine();
    console.log("Car is ready to go!");
  }

  #igniteEngine() {
    console.log("Engine ignited.");
  }
}

const myCar = new Car();
myCar.start(); // "Engine ignited." + "Car is ready to go!"
// myCar.#igniteEngine(); // Error: private method
```

