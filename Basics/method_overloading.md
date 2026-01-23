
**Definition:**

**Method overloading** in Java is a feature that allows multiple methods to have the *same name* but with *different
parameter lists*. It helps improve code readability and allows similar operations to be performed using the same method
name.

Method overloading is also known as `compile-time polymorphism`.

---

**Why Method Overloading is Used:**

• Improves code readability  
• Reduces the need to create multiple method names  
• Makes programs easier to understand and maintain  
• Allows performing similar operations in different ways  

---

**Rules for Method Overloading:**

For methods to be overloaded, at least one of the following must be different:

• Number of parameters  
• Data type of parameters  
• Order of parameters  

Changing only the *return type* is NOT sufficient for method overloading.

---

**1. Overloading by Number of Parameters -**

Example:

class MethodOverloadingExample
{
    static int add(int a, int b)
    {
        return a + b;
    }

    static int add(int a, int b, int c)
    {
        return a + b + c;
    }

    public static void main(String[] args)
    {
        System.out.println(add(5, 10));
        System.out.println(add(5, 10, 15));
    }
}

**Output:**

15  
30  

---

**2. Overloading by Data Type of Parameters -**

Example:

class MethodOverloadingDataType
{
    static int multiply(int a, int b)
    {
        return a * b;
    }

    static double multiply(double a, double b)
    {
        return a * b;
    }

    public static void main(String[] args)
    {
        System.out.println(multiply(4, 5));
        System.out.println(multiply(2.5, 3.0));
    }
}

**Output:**

20  
7.5  

---

**3. Overloading by Order of Parameters -**

Example:

class MethodOverloadingOrder
{
    static void display(int number, char ch)
    {
        System.out.println(number + " " + ch);
    }

    static void display(char ch, int number)
    {
        System.out.println(ch + " " + number);
    }

    public static void main(String[] args)
    {
        display(10, 'A');
        display('B', 20);
    }
}

**Output:**

10 A  
B 20  

---

**Important Points to Remember -**

• Method overloading happens at *compile time*  
• Method name must be the same  
• Parameter list must be different  
• Return type alone cannot overload a method  
• It works for both static and non-static methods  

---

**Summary:**

• Method overloading allows multiple methods with the same name  
• It improves flexibility and readability of code  
• Overloading depends on method parameters, not return type  
• It is a core Java feature and widely used in programs
