
**Data Types :**

In Java, data types define the type of values a variable can store. Java is a strongly typed language, which means every variable
must have a type declared before use.

Java data types are divided into two categories:

• *Primitive Data Types*
• *Non-Primitive Data Types*


• short → 2 bytes, range: -32,768 to 32,767
• int → 4 bytes, range: -2,147,483,648 to 2,147,483,647
• 
Example :

class DataTypesExample
{
public static void main(String args[])
  {
       *Integer types*
        byte b = 100;
        short s = 30000;
        int ("Int: " + i);
     
   
   }
}

2.**Non-Primitive Data Types -**

Non-primitive types (also called reference types) are more complex and are created using classes. They do not store the actual 
value directly; instead, they store a reference (memory address).

Common Non-Primitive Data Types -

• String – sequence of characters
• Arrays – collection of elements of the same type



class NonPrimitiveExample
{
public static void main(String args[])
  {
 
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
