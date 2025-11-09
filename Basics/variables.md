
**Definition:**

A **variable** in Java is a **named memory location** used to store data during the execution of a program. It acts as a 
container that holds values which can be changed, read, or updated while the program runs. Variables make it easy for 
programmers to work with data dynamically instead of using fixed or hard-coded values. In Java, every variable must be 
declared with a **data type**, which tells the compiler what kind of data the variable will hold (such as integer, float, 
character, etc.). The data type also defines the amount of memory allocated to the variable and the operations that can be 
performed on it.

**Declaration & Initialization of Variables -**

A variable is declared by specifying its data type followed by its name. You can also assign (initialize) a value to it 
either during declaration or later in the program.

**Example:**

‣ int age;             // Declaration
‣ age = 20;           // Initialization
‣ int marks = 85;    // Declaration + Initialization

Here, `int` defines the type of variable, `age` is the variable name, and `20` is the value stored in it.

**Naming Rules for Variables:**

‣ Variable names must start with a **letter**, **$**, or **_** (underscore).
‣ They **cannot start with a digit**.
‣ They are **case-sensitive** (`Score` and `score` are different).
‣ Keywords like `int`, `class`, `static`, etc., **cannot** be used as variable names.
‣ Variable names should be **meaningful** and follow **camelCase** convention.

  Example: `studentName`, `totalMarks`.

**Types of Variables in Java:**

Variables in Java are mainly divided into **three categories** based on their **scope**, **lifetime**, and **where they 
are declared** —

1️) Local Variables
2️) Instance Variables
3️) Static (or Class) Variables

**1. Local Variables -**

Local variables are declared **inside a method, constructor, or block**.
They are created when the method starts and destroyed when the method ends.
They can be used **only within that block** and are not accessible outside it.

**Example:**

public void display() 
{
    int number = 10;  // Local variable
    System.out.println(number);
}

Here, `number` exists only while the `display()` method is running. If you try to use it outside the method, an error occurs.

**2. Instance Variables -**

Instance variables are declared **inside a class but outside any method, constructor, or block**.
They are **non-static**, meaning each object of the class gets its own separate copy of the variable.
They are used to represent the state or properties of an object.

**Example:**

class Student 
{
    String name;  // Instance variable
    int age;
    void show() 
    {
        System.out.println(name + " is " + age + " years old.");
    }
}

Each object of `Student` will have its own values for `name` and `age`.

**3. Static (Class) Variables -**

Static variables are declared with the **`static` keyword** inside a class but outside methods.
They belong to the **class itself** rather than any specific object, meaning all objects of that class share the same 
static variable. They are often used for constants or shared properties.

**Example:**

class Student
{
    static String schoolName = "ABC High School";  // Static variable
}

All `Student` objects will share the same `schoolName`. It can be accessed as `Student.schoolName`.

**Variable Scope and Lifetime -**

‣ **Scope** defines where a variable can be accessed in the program.
  Local variables have a limited scope (inside methods), while instance and static variables have a class-level scope.
‣ **Lifetime** defines how long the variable exists in memory.

  Local variables exist temporarily during method execution, while instance variables exist as long as the object exists, 
  and static variables exist for the entire program duration.

**Default Values of Variables -**

In Java, **local variables do not have default values** — you must initialize them before use.
However, **instance and static variables** automatically receive default values depending on their data type.

For example:

| Data Type              | Default Value |
| ---------------------- | ------------- |
| byte, short, int, long | 0             |
| float, double          | 0.0           |
| char                   | '\u0000'      |
| boolean                | false         |
| Object references      | null          |

**Final Variables (Constants) -**

If you declare a variable with the **`final`** keyword, its value **cannot be changed** once assigned.
It becomes a **constant**. This is useful when you want a fixed value throughout the program.

**Example:**

final double PI = 3.14159;
Here, `PI` always remains the same and cannot be modified later.

**In Short:**

| Type         | Declared Inside               | Keyword  | Accessible By      | Default Value           | Example             |
| ------------ | ----------------------------- | -------- | ------------------ | ----------------------- | ------------------- |
| **Local**    | Method / Block                | None     | Only inside method | None (must be assigned) | `int a = 10;`       |
| **Instance** | Inside Class (outside method) | None     | Object             | Depends on type         | `String name;`      |
| **Static**   | Inside Class (outside method) | `static` | Class              | Depends on type         | `static int count;` |

**Summary:**

In short, **variables are the backbone of any Java program**. They help store, manipulate, and reuse data efficiently. 
By understanding their types, scope, and lifetime, you can write programs that are cleaner, more efficient, and 
easy to maintain.
