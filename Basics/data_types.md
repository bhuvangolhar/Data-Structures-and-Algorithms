
**Data Types :**

In Java, data types define the type of values a variable can store. Java is a strongly typed language, which means every variable
must have a type declared before use.

Java data types are divided into two categories:

• *Primitive Data Types*
• *Non-Primitive Data Types*

1.**Primitive Data Types -**

Primitive data types are the most basic data types built into Java. They store simple values directly in memory.

Types of Primitive Data Types -

• byte → 1 byte, range: -128 to 127
• short → 2 bytes, range: -32,768 to 32,767
• int → 4 bytes, range: -2,147,483,648 to 2,147,483,647
• long → 8 bytes, range: huge integers, used with L suffix
• float → 4 bytes, decimal values, up to 7 digits precision (use f suffix)
• double → 8 bytes, decimal values, up to 15 digits precision (default for decimals)
• char → 2 bytes, stores a single character (uses Unicode)
• boolean → 1 bit, stores true or false

Example :

class DataTypesExample
{
public static void main(String args[])
  {
       *Integer types*
        byte b = 100;
        short s = 30000;
        int i = 100000;
        long l = 1000000000L;
       *Floating types*
        float f = 12.34f;
        dou + b);
        System.out.println("Short: " + s);
        System.out.println("Int: " + i);
        System.out.println("Long: " + l);
        System.out.println("Float: " + f);
        System.out.println("Double: " + d);
        System.out.println("Char: " + c);
        System.out.println("Boolean: " + flag);
   }
}

2.**Non-Primitive Data Types -**

Non-primitive types (also called reference types) are more complex and are created using classes. They do not store the actual 
value directly; instead, they store a reference (memory address).

Common Non-Primitive Data Types -

• String – sequence of characters
• Arrays – collection of elements of the same type
• Classes – user-defined blueprints for objects
• Objects – instances of classes
• Interfaces – abstraction mechanism

Example :

class NonPrimitiveExample
{
public static void main(String args[])
  {
   *String*
    String name = "Java";
    *Array*
    int arr[] = {1, 2, 3, 4, 5};
    *Object*
    NonPrimitiveExample obj = new NonPrimitiveExample();
    System.out.println("String: " + name);
    System.out.println("Array first element: " + arr[0]);
    System.out.println("Object reference: " + obj);
  }
}

Key Differences -

1) Primitive types are predefined and faster.
2) Non-primitive types are created by programmers or provided by Java API.
3) Primitive stores value directly, Non-primitive stores reference (address).
4) Primitive types start with lowercase (int, char), Non-primitive types start with uppercase (String, Array).
