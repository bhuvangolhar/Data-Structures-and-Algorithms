----
**Definition:**

An **`object`** in Java is a real-world entity or an instance of a class. It represents something that has both state
(data/attributes) and behavior (actions/methods). When a class is defined, it acts only as a blueprint — no memory is 
allocated until an object of that class is created. Once an object is created, it contains its own copy of the variables 
defined in the class and can use the class’s methods to perform actions. In simpler terms, a class defines *what an object 
is?*, while the object represents a specific example of that class in memory.

**Characteristics of an Object:**

1) **Identity -**
   Each object has a unique identity that distinguishes it from other objects (even if they hold the same data).

2) **State -**
   The data or attributes (variables) that define the current condition of the object.
   Example: `model = "Tesla", year = 2024`

3) **Behavior -**
   The actions or operations the object can perform, defined by methods in the class.
   Example: `start()`, `brake()`, etc.

**Syntax to Create an Object:**

ClassName objectName = new ClassName();

Here,

▫ `ClassName` – the class from which the object is created.
▫ `objectName` – reference variable that stores the object’s address.
▫ `new` – keyword that allocates memory for the object.
▫ `ClassName()` – calls the class constructor to initialize the object.

**Example:**

class Car 
{
    String model;
    int year;
    void start() 
    {
        System.out.println(model + " (" + year + ") is starting...");
    }
}
class Example 
{
    public static void main(String[] args) 
    {
        // Creating an object of Car
        Car c1 = new Car();
        // Assigning values to object properties
        c1.model = "Tesla";
        c1.year = 2024;
        // Calling method using object
        c1.start();
    }
}

**Output:**

Tesla (2024) is starting...

**Key Points about Objects:**

▫ Objects are created using the **`new`** keyword.
▫ Each object has its own copy of instance variables but can share class (static) variables.
▫ Multiple objects can be created from a single class.
▫ Objects interact with each other by calling methods.
▫ Without objects, classes cannot be used in a running Java program.

In summary, an object is the heart of object-oriented programming in Java — it brings classes to life 
by turning blueprints into working, interactive components of a program.
