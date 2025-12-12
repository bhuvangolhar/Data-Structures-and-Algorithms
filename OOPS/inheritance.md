=

**Definition:**

**Inheritance** in Java is one of the core principles of Object-Oriented Programming System (OOPs). It allows one 
class (called the child class or subclass) to acquire the properties and behaviors (fields and methods) of another 
class (called the parent class or superclass). The main purpose of inheritance is code reusability — it allows you 
to use existing code without rewriting it, while also enabling you to extend or modify it as needed. It also helps 
establish a hierarchical relationship between classes, similar to real-world relationships (for example, a “Car” is 
a type of “Vehicle”). Inheritance is a mechanism in Java by which one class can inherit fields and methods of another 
class using the extends keyword.

**Syntax:**

class ParentClass 
{
    // parent class members
}
class ChildClass extends ParentClass 
{
    // child class members
}

Here,

• `ParentClass` → the superclass (base class).
• `ChildClass` → the subclass (derived class).
• The subclass automatically inherits all accessible members `(variables & methods)` of the superclass.

**Example:**

// Parent class
class Animal 
{
    void eat() 
    {
        System.out.println("This animal eats food.");
    }
}
// Child class
class Dog extends Animal 
{
    void bark() 
    {
        System.out.println("The dog barks.");
    }
}
class Example 
{
    public static void main(String[] args) 
    {
        Dog d = new Dog();
        d.eat();   // Inherited method from Animal
        d.bark();  // Method of Dog class
    }
}

**Output:**

This animal eats food.
The dog barks.

**Explanation:**

• The **`Animal`** class is the **superclass**, and `Dog` is the **subclass**.
• The subclass `Dog` automatically **inherits** the method `eat()` from the superclass `Animal`.
• The subclass can also define its own additional methods (like `bark()`).

**Types of Inheritance in Java:**

1] **Single Inheritance -**
   A subclass inherits from only one superclass.
   *(Supported in Java)*

2] **Multilevel Inheritance -**
   A class is derived from another derived class.
   Example: `Class C extends Class B; Class B extends Class A;`
   *(Supported in Java)*

3] **Hierarchical Inheritance -**
   Multiple subclasses inherit from a single superclass.
   *(Supported in Java)*

4] **Multiple Inheritance (through classes) -**
   One class inherits from multiple classes.
   *(Not supported directly in Java)* — Java avoids this to prevent ambiguity, but it can be achieved using **interfaces**.

**Key Points about Inheritance:**

• Achieved using the **`extends`** keyword (for classes) and `implements` (for interfaces).
• Promotes code reuse, maintainability, and scalability.
• A subclass can override methods of its superclass to provide specific behavior (known as method overriding).
• The **`super`** keyword is used to refer to the parent class — for calling parent constructors or methods.
• Constructors are not inherited, but the subclass constructor can call the superclass constructor using `super()`.
• In Java, all classes implicitly inherit from the `Object` class (the root of all classes).

**Example of Multilevel Inheritance:**

class Animal 
{
    void eat() 
    {
         System.out.println("Eating..."); 
    }
}
class Dog extends Animal 
{
    void bark() 
    { 
         System.out.println("Barking..."); 
    }
}
class Puppy extends Dog 
{
    void weep() 
    {
         System.out.println("Weeping..."); 
    }
}
class Example 
{
    public static void main(String[] args) 
    {
        Puppy p = new Puppy();
        p.eat();   // from Animal
        p.bark();  // from Dog
        p.weep();  // from Puppy
    }
}

**Output:**

Eating...
Barking...
Weeping...

**Advantages:**

• **Code Reusability -** Avoids rewriting the same code multiple times.
• **Extensibility -** Allows adding new features without modifying existing code.
• **Maintainability -** Easier to manage and update code in large projects.
• **Polymorphism Support -** Enables method overriding for runtime flexibility.

In summary, **inheritance** in Java provides a way to reuse and extend existing classes, build logical hierarchies, 
and write cleaner, more organized, and efficient object-oriented programs.
