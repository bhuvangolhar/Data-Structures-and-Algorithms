!!!.

**Definition:**

**Polymorphism** is one of the core concepts of Object-Oriented Programming System (OOPs) in Java. The word 
*“Polymorphism”* comes from two Greek words — “poly” (many) and “morph” (forms) — meaning `“many forms.”` 
In simple terms, polymorphism allows one object or method to behave in multiple ways depending on the context. 
It enables the same method name or operator to perform different actions based on the type of object that it is 
acting upon. Polymorphism in Java is the ability of an object to take many forms, allowing the same method or 
interface to represent different behaviors at runtime or compile time.

**Key Idea:**

Polymorphism lets you write flexible, reusable, and maintainable code. It’s what allows a single method name to be 
used for different types of objects — and Java automatically decides which version of the method to call.

**Types of Polymorphism in Java:**

1. **Compile-Time Polymorphism (Static Binding) -**

   • Achieved through method overloading.
   • The method to be executed is determined at compile time.
   • Example: Same method name but different parameter lists within a class.

2. **Run-Time Polymorphism (Dynamic Binding) -**

   • Achieved through method overriding.
   • The method to be executed is determined at runtime, based on the object’s actual type.
   • Example: A subclass provides a specific implementation of a method already defined in its superclass.

**Example (Compile-Time Polymorphism) [Method Overloading]:**

class MathOperation 
{
    // Method with one parameter
    int add(int a) 
    {
        return a + 10;
    }
    // Overloaded method with two parameters
    int add(int a, int b) 
    {
        return a + b;
    }
}
class Example 
{
    public static void main(String[] args) 
    {
        MathOperation obj = new MathOperation();
        System.out.println(obj.add(5));          // Calls method with one argument
        System.out.println(obj.add(5, 10));     // Calls method with two arguments
    }
}

**Output:**

15
15

**Explanation:**

The compiler determines *which method to call* based on the number of arguments, so this is 
compile-time polymorphism.

**Example (Run-Time Polymorphism) [Method Overriding]:**

class Animal 
{
    void sound() 
    {
        System.out.println("Animal makes a sound");
    }
}
class Dog extends Animal 
{
    // Overriding the method of parent class
    void sound() 
    {
        System.out.println("Dog barks");
    }
}
class Cat extends Animal 
{
    void sound() 
    {
        System.out.println("Cat meows");
    }
}
class Example 
{
    public static void main(String[] args) 
    {
        Animal a;           // Reference variable of parent class
        a = new Dog();      // Object of Dog class
        a.sound();          // Calls Dog’s version
        a = new Cat();      // Object of Cat class
        a.sound();          // Calls Cat’s version
    }
}

**Output:**

Dog barks
Cat meows

**Explanation:**

Although the variable `a` is of type `Animal`, the method that gets executed depends on the actual object type 
(`Dog` or `Cat`) at runtime — hence it’s runtime polymorphism.

**Advantages:**

1) **Code Reusability -** Common interfaces and methods can be used across multiple classes.
2) **Flexibility and Extensibility -** Behavior can easily be extended or modified without changing existing code.
3) **Maintainability -** Reduces redundancy and improves readability.
4) **Dynamic Behavior -** Makes programs adaptable by deciding the appropriate behavior at runtime.

**Real-Life Analogy:**

Imagine the `"makeSound()"` action —

• When applied to a **Dog**, it barks.
• When applied to a **Cat**, it meows.
• When applied to a **Cow**, it moos.

The action (method) is the same, but the behavior (output) depends on the actual object — this is 
`polymorphism in action`.

**Key Points:**

• Polymorphism allows the same interface or method to represent different behaviors.
• Overloading means Compile-time polymorphism.
• Overriding means Runtime polymorphism.
• Achieved mainly through inheritance and method overriding.
• Enhances flexibility, scalability, and clarity in Java applications.

**In Summary:**

**Polymorphism** in Java allows one interface or method name to be used for different underlying forms (data types). 
It enables objects to behave differently based on their actual type — a core reason why Java is powerful, flexible, 
and object-oriented.
