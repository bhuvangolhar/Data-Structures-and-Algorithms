
 **Polymorphism in Java**

**Definition**

* **Polymorphism** means *many forms*.
* In Java, polymorphism allows the **same entity (method or object)** to behave differently in different contexts.
* It is one of the **four pillars of Object-Oriented Programming (OOPs)** (along with Inheritance, Encapsulation, and Abstraction).

   * Achieved through **method overriding** (child class provides a new implementation of a parent class method).

 **Example**

class Calculator {
    // Add two integers
    public int add(int a, int b) {
        return a + b;
    }

   

class Animal {
    public void sound() {
        
    }
}

class Dog extends Animal {
  

}

class Cat extends Animal {
    @Override
    public void sound() {
        System.out.println("Cat meows");
    }
}

public class OverridingDemo {
 

1. **Code Reusability** – Same interface, different implementations.
2. **Flexibility** – Easy to extend and modify programs.
3. **Maintainability** – Clean and modular code.
4. **Dynamic Behavior** – Program behavior can be determined at runtime.

 **Example: Bank Account with Runtime Polymorphism**

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
