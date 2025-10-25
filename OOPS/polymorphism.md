
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

   * The method call is resolved **a
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

