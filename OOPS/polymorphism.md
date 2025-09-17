
 **Polymorphism in Java**

 **Definition**

* **Polymorphism** means *many forms*.
* In Java, polymorphism allows the **same entity (method or object)** to behave differently in different contexts.
* It is one of the **four pillars of Object-Oriented Programming (OOPs)** (along with Inheritance, Encapsulation, and Abstraction).


 **Types of Polymorphism in Java**

1. **Compile-time Polymorphism (Static Binding / Method Overloading)**

   * The method call is resolved **at compile time**.
   * Achieved through **method overloading** (same method name with different parameter lists).

2. **Runtime Polymorphism (Dynamic Binding / Method Overriding)**

   * The method call is resolved **at runtime**.
   * Achieved through **method overriding** (child class provides a new implementation of a parent class method).

 **1. Compile-time Polymorphism (Method Overloading)**

 **Example**

class Calculator {
    // Add two integers
    public int add(int a, int b) {
        return a + b;
    }

   
    }
}

public class OverloadingDemo {
    public static void main(String[] args) {
        Calculator calc = new Calculator();

class Dog extends Animal {
    @Override
    public void sound() {
        System.out.println("Dog barks");
    }
}

class Cat extends Animal {
    @Override
    public void sound() {
        System.out.println("Cat meows");
    }
}

public class OverridingDemo {
    public static void main(String[] args) {
        Animal a1 = new Dog(); // Upcasting
        Animal a2 = new Cat();

        a1.sound();  // Runtime decision → Dog barks
        a2.sound();  // Runtime decision → Cat meows
    }
}

**Output:**


Dog barks
Cat meows


 The method call is decided **at runtime** based on the object type, not the reference type.


**Real-Life Analogy**

* **Compile-time polymorphism:** A **Swiss army knife** — one tool (method name), many uses depending on the situation (different parameters).
* **Runtime polymorphism:** A **remote control** — the button (`sound()` method) is the same, but the device (object type: TV, AC, Music System) decides what actually happens.


 **Advantages of Polymorphism**

1. **Code Reusability** – Same interface, different implementations.
2. **Flexibility** – Easy to extend and modify programs.
3. **Maintainability** – Clean and modular code.
4. **Dynamic Behavior** – Program behavior can be determined at runtime.


## **Example: Bank Account with Runtime Polymorphism**


class Bank {
    public double getRateOfInterest() {
        return 0.0;
    }
}

class SBI extends Bank {
    @Override
    public double getRateOfInterest() {
        return 5.5;
    }
}

class HDFC extends Bank {
    @Override
    public double getRateOfInterest() {
        return 6.8;
    }
}

public class BankDemo {
    public static void main(String[] args) {
        Bank b1 = new SBI();
        Bank b2 = new HDFC();

        System.out.println("SBI Interest Rate: " + b1.getRateOfInterest());
        System.out.println("HDFC Interest Rate: " + b2.getRateOfInterest());
    }
}

**Output:**

SBI Interest Rate: 5.5
HDFC Interest Rate: 6.8


 **When to Use Polymorphism**

* When the same action must be performed differently for different objects.
* When designing **frameworks and APIs** that should be extensible.
* Whenever you want to achieve **loose coupling** in your code.


 **Conclusion**

* **Polymorphism** means *many forms*.
* **Compile-time polymorphism** → achieved by **method overloading**.
* **Runtime polymorphism** → achieved by **method overriding**.
* It improves **flexibility, scalability, and maintainability** of Java applications.

