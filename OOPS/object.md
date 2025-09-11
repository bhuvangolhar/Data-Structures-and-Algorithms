
 **Objects in Java**

**Definition**

* An **object** in Java is an instance of a class.
* While a **class** is like a blueprint or template, an object is the real-world entity created from that blueprint.
* Objects represent entities with **state (data/attributes)** and **behavior (methods/functions)**.


**Why Objects are Needed?**

* Objects allow **real-world modeling**: You can represent things like a *Car, Student, Employee, or Bank Account*.
* They provide **encapsulation**, meaning data and related behavior are bundled together.
* Objects make the program more **modular, reusable, and organized**.
* They help implement the **core principles of OOP**: abstraction, encapsulation, inheritance, and polymorphism.


 **Characteristics of an Object**

1. **Identity** → Each object is unique, even if it has the same state as another.
   Example: Two `Car` objects with the same color and model are still different objects in memory.

2. **State** → The data stored inside an object (fields/variables).
   Example: A `Car` object’s state may include 

3. **Behavior** → The actions an object can perform (methods).
   Example: A `Car` object can `start()`, `stop()`, `accelerate()`.

---

 **Syntax**

To create an object, we use the `new` keyword:

```java
ClassName obj = new ClassName();
```



**Examples**

 Example 1: Simple Object Creation


}

public class ObjectsDemo {
    public static void main(String[] args) {
        // Creating objects
        Student s1 = new Student();
        Student s2 = new Student();

        // Initializing object data
        s1.name = "Bhuvan";
        s1.age = 22;
        
        s2.name = "Riya";
        s2.age = 21;

        // Calling methods on objects
        s1.display();
        s2.display();
    }
}
```

**Output:**

```
Student Name: Bhuvan, Age: 22
Student Name: Riya, Age: 21
```

 **How Objects are Created in Java**

1. **Using `new` keyword** (most common).

   ```java
   Student s1 = new Student();
   ```
2. **Using `newInstance()` method** of `Class` class.
3. **Using clone() method** (copies an existing object).
4. **Using deserialization** (re-creating object from a file/stream).


**Rules for Objects**

* You cannot use an object without first creating it (otherwise you’ll get `NullPointerException`).
* An object reference can point to **null**.
* Multiple references can point to the same object.
* Objects are stored in the **heap memory** in Java.

---
 **Objects in Real Life**

Think of a **class** as a "blueprint of a house" and **objects** as "actual houses built using that blueprint".

* Class = Plan of Car
* Object = Red Maruti Suzuki Car with specific speed, model, and engine.

---

 **Program: Multiple Objects**

```java
class Car {
    String brand;
    int speed;

    void showDetails() {
        System.out.println("Brand: " + brand + ", Speed: " + speed + " km/h");
    }
}

public class ObjectsExample {
    public static void main(String[] args) {
        Car c1 = new Car();
        Car c2 = new Car();

        c1.brand = "BMW";
        c1.speed = 220;

        c2.brand = "Maruti";
        c2.speed = 120;

        c1.showDetails();
        c2.showDetails();
    }
}
```

**Output:**

```
Brand: BMW, Speed: 220 km/h
Brand: Maruti, Speed: 120 km/h
```

---

**Conclusion**

* Objects are the **core building blocks** of Object-Oriented Programming in Java.
* They represent **real-world entities** with **state and behavior**.
* Understanding objects is crucial for mastering **OOP concepts** like inheritance, polymorphism, and encapsulation.

