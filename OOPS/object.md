
 **Objects in Java**

**Definition**

* An **object** in Java is an instance of a class.
* While a
---

}

public class ObjectsDemo {
    public static void main(String[] args) {
        // Creating objects
        Student s1 = 
Student Name: Bhuvan, Age: 22
Student Name: Riya, Age: 21

2. **Using `newInstance()` method** of `Class` class.
3. **Using clone() method** (copies an existing object).
4. **Using deserialization** (re-creating object from a file/stream).


**Rules for Objects**

* You cannot use an object without first creating it (otherwise you’ll get `NullPointerException`).
* An object reference cap memory** in Java.

---
 **Objects in Real Life**

Think of a **class** as a "blueprint of a house" and **objects** as "actual houses built using that blueprint".

* Class = Plan of Car
* Object = Red Maruti Suzuki Car with specific speed, model, and engine.

---

 **Program: Multiple Objects**

```java

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
building blocks** of Object-Oriented Programming in Java.
* They represent **real-world entities** with **state and behavior**.
* Understanding objects is crucial for mastering **OOP concepts** like inheritance, polymorphism, and encapsulation.

