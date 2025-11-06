
 **Inheritance in Java**

**Definition**


class Parent {
    // fields and methods
}

claterfaces only)**

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


