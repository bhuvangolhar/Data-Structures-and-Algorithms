o
**Definition:**

A **class** in Java is the blueprint, template, or prototype from which objects are created. It is a logical 
structure that defines the data (variables) and the **behavior (methods) that the objects of that class will have.
In simpler terms, a class defines *what an object is* and *how it behaves* — but it doesn’t occupy memory until an 
object is created from it. A class represents a concept, while objects represent real instances of that concept. 
A class is a user-defined data type that serves as a model for creating multiple objects with similar properties 
and functions. It allows grouping related variables and methods into a single unit, promoting encapsulation, 
reusability, and clarity in programming.

**Syntax of a Class:**

class ClassName 
{
    // Data members (variables)
    // Member functions (methods)
}

**Example:**

class Car 
{
    // Data members (attributes)
    String model;
    int year;
    // Member function (method)
    void start() 
    {
        System.out.println(model + " (" + year + ") is starting...");
    }
}
class Example 
{
    public static void main(String[] args) 
    {
        // Creating objects of class Car
        Car c1 = new Car();
        c1.model = "Tesla";
        c1.year = 2024;
        c1.start();
    }
}

**Output:**

Tesla (2024) is starting...

**Explanation:**

▪ **`class Car`** – defines a blueprint named `Car`.
▪ **`String model; int year;`** – these are data members (attributes) representing the state of a car.
▪ **`void start()`** – defines a behavior (method) that performs an action.
▪ **`new Car()`** – creates an object of the class, which now has its own data and can perform the defined actions.

**Components of a Class:**

a) **Fields (Variables) -** store the object’s data or attributes.
b) **Methods -** define the actions or behavior of the object.
c) **Constructors -** special methods used to initialize objects when they are created.
d) **Blocks -** used for grouping statements and controlling execution flow.
e) **Nested Classes/Interfaces -** classes defined within another class.

**Key Points about Classes:**

▪ A class does not occupy memory until an object is created.
▪ One class can create multiple objects with different data values.
▪ Classes support encapsulation by combining data and behavior.
▪ They are the foundation of OOPs in Java — every program must have at least one class.
▪ The file name and class name should match if the class is public 
  (e.g., `public class Example` must be in `Example.java`).

In summary, a **class** in Java defines the **structure & behavior** of objects and acts as the building block of all 
object-oriented programming concepts in Java. It provides a clean and organized way to model real-world entities in code.
