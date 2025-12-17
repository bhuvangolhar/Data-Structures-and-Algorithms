`

**Definition:**

A **method** in Java is a block of code that performs a specific task and is executed only when it is called. It helps make
programs organized, reusable, and easy to maintain. Instead of writing the same set of instructions multiple times, you can 
define a method once and call it whenever needed. Every method in Java must be written inside a class.

**Structure of a Method -**

A method generally has five main parts — **access modifier**, **return type**, **method name**, **parameters**, 
and **method body**.

Example:

public int add(int a, int b)
{
    return a + b;
}

Explanation:

•  **public** → access modifier (decides visibility of the method)
•  **int** → return type (specifies what the method will return)
•  **add** → method name
•  **(int a, int b)** → parameters (input values)
•  Code inside `{ }` → method body (statements to execute when the method is called)

**Calling a Method -**

To use a method, it must be called using its name followed by parentheses.
If the method is `static`, it can be called directly using the class name; otherwise, you must create an object.

Example:

• int result = add(10, 20);         // calling a static method
• Calculator c = new Calculator();  // creating object
• c.add(10, 20);                    // calling non-static method

**Types of Methods in Java -**

Java methods can be classified in several ways based on their purpose and usage.

**1. Predefined Methods:**

These are methods already defined in Java’s standard library. They are also called **built-in methods** and are ready to use.

Example:

• System.out.println("Hello Java");  // println() is predefined
• int len = "Hello".length();       // length() is predefined

They make programming easier because you don’t have to write common logic manually.

**2. User-Defined Methods:**

These are methods created by the programmer to perform specific tasks.

Example:

void greet()
{
    System.out.println("Good Morning!");
}

This method can be called whenever you want to display the message.

**Static and Non-Static Methods -**

a)  **Static Method:** 

Belongs to the class and can be called without creating an object.

   class Demo
  {
      static void display()
      {
          System.out.println("Static Method");
      }
  }
  Demo.display();

b) **Non-Static Method:** 

Belongs to an object and needs an object to be called.

  class Demo
  {
      void show()
      {
          System.out.println("Non-Static Method");
      }
  }
  Demo d = new Demo();
  d.show();

**Methods Based on Parameters and Return Type -**

Java methods can also be classified based on whether they accept inputs (parameters) and whether they return a value.

**1. Non-Parameterized Method (No Parameters):**

These methods do not take any input. The code runs the same way every time it’s called.

void displayMessage()
{
    System.out.println("Welcome to Java!");
}

**2. Parameterized Method:**

These methods take input values (parameters) that allow the same method to work with different data.

void greetUser(String name)
{
    System.out.println("Hello, " + name + "!");
}

If you call `greetUser("Bhuwan");`, it will print **Hello, Bhuvan!**

**3. Method with Return Type:**

A method can return a value using the `return` keyword. The data type of the returned value must match the declared return 
type.

int square(int n)
{
    return n * n;
}

Here, the method returns an integer value that can be stored or used later.

**4. Void Method (No Return Value):**

If a method does not return any value, its return type is written as `void`.

void sayHello() 
{
    System.out.println("Hello World!");
}

This method performs an action but does not give back any value.

**Benefits of Using Methods -**

Methods make code modular, reusable, and easy to debug. They allow programmers to divide a large program into 
smaller parts, improving readability and reducing redundancy. Updating or fixing one method doesn’t affect the rest of the 
program, which makes maintenance easier.

**In Short:**

| Type              | Description                       | Example                  |
| ----------------- | --------------------------------- | ------------------------ |
| Predefined        | Already available in Java library | `System.out.println()`   |
| User-Defined      | Created by the programmer         | `void greet()`           |
| Static            | Called without object             | `ClassName.methodName()` |
| Non-Static        | Called using an object            | `obj.methodName()`       |
| Parameterized     | Accepts input values              | `int add(int a, int b)`  |
| Non-Parameterized | No input                          | `void show()`            |
| Returning         | Returns a value                   | `return x + y;`          |
| Void              | Does not return any value         | `void printMsg()`        |
