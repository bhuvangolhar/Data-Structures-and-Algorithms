

 *Class in Java*

**Definition**

* A **class** in Java is a **blueprint (template)** for creating objects.
* It defines the **data (fields/variables)** and the **behavior (methods)** that the objects created from it will have.
* While objects are the actual entities in memory, the **class is just the definition** of what those entities will look like.



 **Why Do We Need Classes?**

* Classes bring **organization and modularity** to Java programs.
* Instead of writing data and logic separately, classes bundle both together**.
* They allow **code reusability** (you can create multiple objects from the same class).
* They are essential for implementing **Object-Oriented Programming concepts** such as inheritance, encapsulation, and polymorphism.


 **Syntax of a Class**


class ClassName {
    // Fields (variables)
    dataType variableName;

    // Methods (functions)
    returnType methodName(parameters) {
        // method body
    }
}




 **Components of a Class**

1. **Fields (Instance Variables)** → Define the state/properties of the class.
   Example: `String name; int age;`

2. **Methods (Member Functions)** → Define the behavior of the class.
   Example: `void display()`

3

class Student {
    // Fields
    String name;
    int age;

    // Method
    void display() {
        System.out.println("Name: " + name + ", Age: " + age);
    }
}

public class ClassDemo {
    public static void main(String[] args) {
        // Creating objects from the Student class
        Student s1 = new Student();
        Student s2 = new Student();

        // Initializing values
        s1.name = "Bhuvan";
        s1.age = 22;

        s2.name = "Riya";
        s2.age = 21;

        // Calling methods
        s1.display();
        s2.display();
    }
}


**Output:**


Name: Bhuvan, Age: 22
Name: Riya, Age: 21


 **Real-World Analogy**

* A **class** is like a **blueprint of a house**.
* An **object** is the **actual house built from that blueprint**.
* You can use the same class (blueprint) to create multiple objects (houses) with different features.



**Types of Classes in Java**

1. **Concrete Class** – A normal class from which objects can be created.
2. **Abstract Class** – A class that cannot be instantiated, but can be extended.
3. **Final Class** – A class that cannot be extended (inherited).
4. **Nested/Inner Class** – A class defined inside another class.
5. **POJO Class** – Plain Old Java Object, a simple class with fields, constructors, and getters/setters.



 **Memory Allocation for Classes**

* When you define a class, **no memory is allocated**.
* Memory is allocated **only when an object is created** using `new`.
* The class is loaded once by the **ClassLoader** into JVM memory.



 **Example 2: Class with Methods**

class Car {
    String brand;
    int speed;

    void start() {
        System.out.println(brand + " is starting...");
    }

    void accelerate(int increase) {
        speed += increase;
        System.out.println(brand + " accelerated to " + speed + " km/h");
    }
}

public class ClassExample {
    public static void main(String[] args) {
        Car c1 = new Car();
        c1.brand = "BMW";
        c1.speed = 100;

        c1.start();
        c1.accelerate(50);
    }
}


**Output:**

BMW is starting...
BMW accelerated to 150 km/h




 **Class vs Object**

| Feature      | Class                                           | Object                             |
| ------------ | ----------------------------------------------- | ---------------------------------- |
| Definition   | Blueprint/template                              | Instance of a class                |
| Existence    | Logical entity (no memory until object created) | Physical entity (stored in memory) |
| Example      | `Student` class                                 | `Student s1 = new Student();`      |
| Multiplicity | One class can create multiple objects           | Each object belongs to some class  |



 **Conclusion**

* A **class is the backbone of OOP in Java**.
* It represents a **blueprint** containing variables and methods.
* Objects are created based on the class, and together they help in building **modular, reusable, and real-world applications**.
