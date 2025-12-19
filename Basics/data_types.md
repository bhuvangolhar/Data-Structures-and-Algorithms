3
**Definition:**

A **data type** in Java defines the kind of data a variable can store and how much memory it needs. It tells the compiler 
what type of value (like number, character, or true/false) will be stored in a variable. Data types are important because 
Java is a *strongly typed language*, meaning every variable must have a defined data type before it is used.

Java data types are broadly divided into two main categories:

1. **Primitive Data Types**
2. **Non-Primitive (Reference) Data Types**

**1. Primitive Data Types:**

Primitive data types are the most basic types built into Java. They directly store simple values in memory and are not 
objects.
There are **eight primitive data types** in Java — `byte`, `short`, `int`, `long`, `float`, `double`, `char`, and `boolean`.

Let’s look at each one in detail,

**a) byte -**

• Used to store very small integer values.
• It saves memory and is often used in large arrays.
• **Size:** 1 byte (8 bits)
• **Range:** -128 to 127

Example:

byte age = 25;

**b) short -**

• Stores small integer values (larger than byte but smaller than int).
• **Size:** 2 bytes (16 bits)
• **Range:** -32,768 to 32,767

Example:

short distance = 1500;

**c) int -**

• The most commonly used data type for integers.
• **Size:** 4 bytes (32 bits)
• **Range:** -2,147,483,648 to 2,147,483,647

Example:

int salary = 50000;

**d) long -**

• Used for very large integer values.
• You must add an **‘L’** or **‘l’** at the end of the value.
• **Size:** 8 bytes (64 bits)
• **Range:** -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807

Example:

long population = 15000000000L;

**e) float -**

• Used for decimal numbers (fractional values).
• Less precise than double.
• You must add an **‘F’** or **‘f’** at the end of the value.
• **Size:** 4 bytes (32 bits)
• **Range:** Approximately ±3.4e38

Example:

float price = 19.99F;

**f) double -**

• Used for large decimal numbers (more precise than float).
• **Size:** 8 bytes (64 bits)
• **Range:** Approximately ±1.7e308

Example:

double marksPercentage = 89.65;

**g) char -**

• Used to store a single character (like a letter or symbol).
• Enclosed in **single quotes (‘ ’)**.
• **Size:** 2 bytes (because Java uses Unicode)
• **Range:** 0 to 65,535

Example:

char grade = 'A';

**h) boolean -**

• Used to store logical values — **true** or **false** only.
• **Size:** 1 bit (true or false)

Example:

boolean isJavaFun = true;

**Summary of Primitive Data Types:**

| Data Type | Size    | Range / Values                  | Example                    |
| --------- | ------- | ------------------------------- | -------------------------- |
| byte      | 1 byte  | -128 to 127                     | `byte a = 10;`             |
| short     | 2 bytes | -32,768 to 32,767               | `short s = 150;`           |
| int       | 4 bytes | -2,147,483,648 to 2,147,483,647 | `int n = 5000;`            |
| long      | 8 bytes | Very large range                | `long l = 123456789L;`     |
| float     | 4 bytes | Up to 7 decimal digits          | `float f = 3.14F;`         |
| double    | 8 bytes | Up to 15 decimal digits         | `double d = 3.1415926535;` |
| char      | 2 bytes | Single character (Unicode)      | `char c = 'A';`            |
| boolean   | 1 bit   | true or false                   | `boolean b = true;`        |

**2. Non-Primitive Data Types OR Reference Data Types:**

Non-primitive data types are more complex and are created by the programmer. They store **references (memory addresses)** of 
actual data rather than the data itself.

Common examples include **Strings, Arrays, Classes, Interfaces, and Objects**.

• **String** → Stores a sequence of characters.
    ex.String name = "Java Programming";

• **Array** → Stores multiple values of the same data type.
    ex.int[] marks = {90, 80, 85};
  
• **Class** → A blueprint for creating objects.
    ex.class Car { } 

• **Object** → An instance of a class.
    ex.Car c = new Car();

• **Interface** → Defines a set of methods that a class must implement. It only provides the structure, 
                  not the implementation.
    ex.interface Animal { void sound(); }

These data types are stored in **heap memory**, and since they are derived from classes, they have methods that can be used
to manipulate data (for example, `length()`, `toUpperCase()`, etc., for Strings).

**In short:**

Primitive data types hold *simple values directly*, while non-primitive types hold *references to objects*. Together, 
they make Java a powerful and type-safe programming language.
