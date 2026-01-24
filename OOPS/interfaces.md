
**Definition:**

An **interface** in Java is a blueprint of a class that contains *`abstract methods`* (methods without a body) and
constants. It is used to achieve "abstraction" and "multiple inheritance" in Java.

An interface defines *what a class should do*, but not *how it should do it*.

---

**Why Interfaces Are Used:**

• To achieve abstraction  
• To support multiple inheritance  
• To define a common contract for classes  
• To improve code flexibility and scalability  

---

**Syntax of an Interface -**

interface InterfaceName
{
    methodDeclarations;
}

A class uses the `implements` keyword to implement an interface.

---

**1. Simple Interface Example -**

Example:

interface Animal
{
    void sound();
}

class Dog implements Animal
{
    public void sound()
    {
        System.out.println("Dog barks");
    }

    public static void main(String[] args)
    {
        Dog d = new Dog();
        d.sound();
    }
}

**Output:**

Dog barks

Here, the `Dog` class provides the implementation of the `sound()` method defined in the `Animal` interface.

---

**2. Interface with Multiple Methods -**

Example:

interface Calculator
{
    int add(int a, int b);
    int subtract(int a, int b);
}

class SimpleCalculator implements Calculator
{
    public int add(int a, int b)
    {
        return a + b;
    }

    public int subtract(int a, int b)
    {
        return a - b;
    }

    public static void main(String[] args)
    {
        SimpleCalculator calc = new SimpleCalculator();
        System.out.println(calc.add(10, 5));
        System.out.println(calc.subtract(10, 5));
    }
}

**Output:**

15  
5  

---

**3. Multiple Inheritance Using Interface -**

Java does not support multiple inheritance using classes, but it supports it using interfaces.

Example:

interface A
{
    void show();
}

interface B
{
    void display();
}

class C implements A, B
{
    public void show()
    {
        System.out.println("Show method from interface A");
    }

    public void display()
    {
        System.out.println("Display method from interface B");
    }

    public static void main(String[] args)
    {
        C obj = new C();
        obj.show();
        obj.display();
    }
}

---

**Rules of Interfaces -**

• All methods are public and abstract by default  
• Variables are public, static, and final by default  
• Interfaces cannot have constructors  
• A class can implement multiple interfaces  
• An interface cannot create objects  

---

**Interface vs Abstract Class -**

| Feature              | Interface                | Abstract Class          |
|----------------------|--------------------------|-------------------------|
| Methods              | Abstract (by default)    | Abstract or concrete    |
| Multiple inheritance | Supported                | Not supported           |
| Variables            | public static final      | Any type                |
| Constructors         | Not allowed              | Allowed                 |
| Keyword used         | implements               | extends                 |

---

**Important Points to Remember -**

• Interfaces provide full abstraction  
• They define *what* a class must do  
• Used widely in real-world Java applications  
• Enable loose coupling between classes  

---

**Summary:**

• Interfaces are used to achieve abstraction  
• They support multiple inheritance  
• A class implements an interface  
• Interfaces improve flexibility and design
