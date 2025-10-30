
 **Inheritance in Java**

**Definition**


class Parent {
    // fields and methods
}

cla


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
  2. **
    }
}

class Child extends Parent {
    int num = 200;

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


## **Method Overriding in Inheritanc **Advantages of Inheritance**

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


