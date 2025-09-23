
 **Inheritance in Java**

**Definition**

* **Inheritance** is one of the four main pillars of Object-Oriented Programming (OOP).
* It allows a **class (child/subclass)** to acquire the **properties (fields)** and **behaviors (methods)** of another class (parent/superclass).


**Key Points**

1. The class that is inherited from is called the **Parent class / Superclass / Base class**.
2. The class that inherits is called the **Child class / Subclass / Derived class**.


**Syntax**

class Parent {
    // fields and methods
}

class Child extends Parent {
    // additional fields and methods
}

**Example 1: Basic Inheritance**





**Types of Inheritance in Java**

Unlike C++ (which supports multiple inheritance via classes), Java supports only **single inheritance with classes** to avoid ambiguity (diamond problem).
However, multiple inheritance is possible with **interfaces**.

1. **Single Inheritance**

One child inherits from one parent.


class Animal { void eat() { System.out.println("Eating..."); } }
class Dog extends Animal { void bark() { System.out.println("Barking..."); } }

 2. **Multilevel Inheritance**

A class inherits from a class which itself inherits from another class.


class Animal { void eat() { System.out.println("Eating..."); } }


### 3. **Hierarchical Inheritance**

Multiple child classes inherit from a single parent class.


class Animal { void eat() { System.out.println("Eating..."); } }
class Dog extends Animal { void bark() { System.out.println("Barking..."); } }
class Cat extends Animal { void meow() { System.out.println("Meowing..."); } }


### 4. **Multiple Inheritance (through interfaces only)**

Java does not allow multiple inheritance with classes, but it allows it with **interfaces**.

interface A { void methodA(); }
interface B { void methodB(); }

class C implements A, B {
    public void methodA() { System.out.println("Method A"); }
    public void methodB() { System.out.println("Method B"); }
}


 **The `super` Keyword**

* Used to refer to the **parent class’s members**.
* Common uses:

  1. **Call parent constructor:** `super()`
  2. **Access parent fields or methods:** `super.fieldName`, `super.methodName()`

**Example:**


class Parent {
    int num = 100;
    void show() {
        System.out.println("Parent show()");
    }
}

class Child extends Parent {
    int num = 200;

    void show() {
        super.show(); // Call parent method
        System.out.println("Parent num: " + super.num); // Access parent variable
        System.out.println("Child num: " + num);
    }
}

public class SuperDemo {
    public static void main(String[] args) {
        Child c = new Child();
        c.show();
    }
}


**Output:**


Parent show()
Parent num: 100
Child num: 200


## **Method Overriding in Inheritance**

* A child class can provide its **own implementation** of a method that already exists in the parent class.
* Achieved by using the **same method name, return type, and parameters**.
* Useful for **runtime polymorphism**.

**Example:**

class Animal {
    void sound() {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

public class OverridingDemo {
    public static void main(String[] args) {
        Animal a = new Dog(); // Upcasting
        a.sound(); // Calls Dog's sound()
    }
}


**Output:**


Dog barks

 **Advantages of Inheritance**

1. **Code reusability** – Common code written once in the parent class can be reused.
2. **Method overriding** – Provides flexibility to modify behavior in child classes.
3. **Polymorphism** – Enables runtime method resolution (dynamic binding).
4. **Organized structure** – Better hierarchy of related classes.

**Limitations of Inheritance**

* **Tight coupling** between parent and child.
* Changes in the parent class may affect all child classes.
* Java supports only **single inheritance with classes** (but allows multiple with interfaces).


**Class Diagram (Example)**

        Animal (Superclass)
           |
   -------------------
   |                 |
  Dog               Cat

 **Conclusion**

* Inheritance is a **powerful mechanism** in Java OOP to build hierarchies, reuse code, and achieve polymorphism.
* Java supports **single, multilevel, and hierarchical inheritance with classes**, and **multiple inheritance with interfaces**.
* Together with **encapsulation and polymorphism**, inheritance makes Java applications **flexible, reusable, and maintainable**.


