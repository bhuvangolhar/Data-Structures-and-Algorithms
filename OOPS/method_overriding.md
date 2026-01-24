
**Definition:**

**Method overriding** in Java occurs when a child class provides its own implementation of a method that is already
defined in its *parent class*. The overridden method must have the same method name, same parameters and same return
type as the method in the parent class.

Method overriding is used to achieve **runtime polymorphism**.

---

**Why Method Overriding is Used:**

• To change the behavior of a parent class method  
• To achieve runtime decision-making  
• To support polymorphism  
• To allow flexible and reusable code  

---

**Basic Example of Method Overriding -**

Example:

class Parent
{
    void show()
    {
        System.out.println("This is the parent class method");
    }
}

class Child extends Parent
{
    void show()
    {
        System.out.println("This is the child class method");
    }

    public static void main(String[] args)
    {
        Child obj = new Child();
        obj.show();
    }
}

**Output:**

This is the child class method

Here, the `show()` method in the child class overrides the `show()` method of the parent class.

---

**Method Overriding Using Parent Reference -**

This example shows that method calls are resolved at **runtime**, not compile time.

Example:

class Parent
{
    void display()
    {
        System.out.println("Display method from Parent class");
    }
}

class Child extends Parent
{
    void display()
    {
        System.out.println("Display method from Child class");
    }

    public static void main(String[] args)
    {
        Parent obj = new Child();
        obj.display();
    }
}

**Output:**

Display method from Child class

This happens because Java decides which method to call based on the object type, not the reference type.

---

**Using `@Override` Annotation -**

The `@Override` annotation is used to indicate that a method is overriding a parent class method. It helps catch errors
during compilation.

Example:

class Parent
{
    void greet()
    {
        System.out.println("Hello from Parent");
    }
}

class Child extends Parent
{
    @Override
    void greet()
    {
        System.out.println("Hello from Child");
    }
}

---

**Rules for Method Overriding -**

• Method name must be the same  
• Parameter list must be the same  
• Return type must be the same or compatible  
• Inheritance is required  
• Overriding happens at runtime  

---

**Methods That Cannot Be Overridden -**

• `final` methods  
• `static` methods  
• `private` methods  

---

**Difference Between Method Overloading and Overriding -**

| Feature            | Method Overloading        | Method Overriding        |
|--------------------|---------------------------|--------------------------|
| Occurs in          | Same class                | Parent and child class  |
| Method name        | Same                      | Same                    |
| Parameters         | Must be different         | Must be same            |
| Binding time       | Compile time              | Runtime                 |
| Inheritance needed | No                        | Yes                     |

---

**Important Points to Remember -**

• Overriding supports runtime polymorphism  
• Child class method is executed instead of parent method  
• Access level cannot be reduced  
• `@Override` helps avoid mistakes  
• Method overriding depends on object creation  

---

**Summary:**

• Method overriding allows redefining parent class behavior  
• It requires inheritance  
• Method call is decided at runtime  
• It is a core concept of Object-Oriented Programming
