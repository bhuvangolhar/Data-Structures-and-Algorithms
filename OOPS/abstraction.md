
**Definition:**

**Abstraction** is one of the four main pillars of Object-Oriented Programming System (OOPs)** in Java (along with 
Encapsulation, Inheritance, and Polymorphism). It focuses on hiding the internal implementation details and showing 
only the essential features of an object or system. In simple words, abstraction allows you to *focus on what an object 
does* rather than *how it does it*. It helps simplify complex systems by breaking them down into more manageable and 
understandable parts.Abstraction in Java is the process of **hiding complex implementation details** and exposing only  
the necessary functionalities to the user. It enables a programmer to use objects, methods, or classes without needing 
to understand their inner workings.

**Key Ideas:**

Abstraction is like using a **TV remote** — you press buttons (methods) to change the channel or volume, but you don’t 
need to know the **complex circuitry** inside the remote.

Java achieves abstraction mainly through:

a] **Abstract classes**, and
b] **Interfaces**.

**a] Abstract Classes -**

An **abstract class** is a class declared with the `abstract` keyword.

▪ It cannot be instantiated directly (i.e., you can’t create objects of it).
▪ It can contain both abstract methods (without implementation) and non-abstract methods (with implementation).
▪ Used when you want to provide a base class that other classes can extend and customize.

**Syntax:**

abstract class ClassName 
{
    abstract void methodName();        // abstract method (no body)
    void normalMethod()                 // concrete method (has body)
    {       
         // code here
    }
}

**Example (Using Abstract Class):**

abstract class Animal 
{
    // Abstract method (no implementation)
    abstract void sound();
    // Non-abstract method
    void sleep() 
    {
        System.out.println("Animal is sleeping...");
    }
}
class Dog extends Animal 
{
    // Providing implementation for abstract method
    void sound() 
    {
        System.out.println("Dog barks");
    }
}
class Example 
{
    public static void main(String[] args) 
    {
        Animal a = new Dog();          // Upcasting
        a.sound();                      // Calls Dog’s implementation
        a.sleep();                       // Calls Animal’s non-abstract method
    }
}

**Output:**

Dog barks
Animal is sleeping...

**Explanation:**

▪ The **abstract class `Animal`** defines a general structure — all animals can “make a sound” and “sleep.”
▪ The **`Dog`** class provides the specific implementation of the `sound()` method.
▪ This helps in hiding details while allowing flexibility for subclasses.

**b] Interfaces -**

An **interface** in Java is a *completely abstract structure* that can contain only abstract methods (until Java 7) 
and default/static methods (from Java 8 onward).

▪ It defines **what a class must do**, not **how** it does it.
▪ A class implements an interface and provides the actual behavior.

**Syntax:**

interface InterfaceName 
{
    void methodName();          // abstract method
}

**Example (Using Interface):**

interface Vehicle 
{
    void start();               // abstract method
}
class Car implements Vehicle 
{
    public void start() 
    {
        System.out.println("Car starts with a key");
    }
}
class Bike implements Vehicle 
{
    public void start() 
    {
        System.out.println("Bike starts with a button");
    }
}
class Example 
{
    public static void main(String[] args) 
    {
        Vehicle v1 = new Car();
        Vehicle v2 = new Bike();
        v1.start();
        v2.start();
    }
}

**Output:**

Car starts with a key
Bike starts with a button

**Explanation:**

▪ The **interface `Vehicle`** defines a common behavior (`start()`), but doesn’t specify how it should be performed.
▪ The **classes `Car` and `Bike`** provide their own implementations.
▪ This ensures **flexibility and abstraction** — different vehicles can behave differently but still follow the 
  same ontract.

**Advantages:**

i) **Simplifies Complex Systems -** Hides unnecessary details and presents only important features.
ii) **Improves Code Readability -** The user interacts only with the essential parts of the system.
iii) **Enhances Reusability -** Abstract classes and interfaces can be reused across multiple classes.
iv) **Promotes Loose Coupling -** Changes in implementation don’t affect other parts of the code.
v) **Encourages Design Flexibility -** Allows multiple implementations for the same interface or abstract class.

**Real-Life Analogy:**

When you `drive a car`, you use the steering wheel, brakes, and accelerator —
but you don’t need to know how the *engine* or *brake mechanism* works internally.
That’s **abstraction** — using functionality without worrying about implementation details.

**Key Points:**

▪ Achieved using abstract classes and interfaces.
▪ Abstract methods provide a structure without defining behavior.
▪ You cannot create objects of an abstract class or interface.
▪ Abstract classes can have both abstract and concrete methods.
▪ Interfaces are ideal for achieving full abstraction.
▪ Abstraction improves security, scalability, and modularity.

**In Summary:**

**Abstraction** in Java focuses on showing only what is necessary and hiding complex details.
It allows programmers to design systems that are clean, organized, and easy to maintain, while ensuring 
that implementation details remain hidden behind well-defined interfaces or abstract classes.
