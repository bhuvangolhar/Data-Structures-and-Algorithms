
**Definition:**

**Exception handling** in Java is a mechanism used to *handle runtime errors* so that the normal flow of a program can be
maintained. An exception is an unexpected event that occurs during program execution and disrupts normal execution.

Java provides built-in support for exception handling using keywords like `try`, `catch`, `finally`, `throw` and
`throws`.

---

**Why Exception Handling Is Needed:**

• Prevents program termination due to runtime errors  
• Allows graceful handling of errors  
• Improves program reliability  
• Separates error-handling code from normal logic  

---

**Types of Exceptions in Java:**

Java exceptions are mainly divided into two types:

1. Checked Exceptions  
2. Unchecked Exceptions  

---

**1. Checked Exceptions -**

Checked exceptions are checked at **compile time**. The programmer must handle them using `try-catch` or `throws`.

Examples:

• IOException  
• SQLException  
• FileNotFoundException  

---

**2. Unchecked Exceptions -**

Unchecked exceptions occur at **runtime** and are not checked during compilation.

Examples:

• ArithmeticException  
• NullPointerException  
• ArrayIndexOutOfBoundsException  

---

**Basic try-catch Example -**

The `try` block contains code that may cause an exception. The `catch` block handles the exception.

Example:

class TryCatchExample
{
    public static void main(String[] args)
    {
        try
        {
            int a = 10 / 0;
        }
        catch (ArithmeticException e)
        {
            System.out.println("Cannot divide by zero");
        }
    }
}

**Output:**

Cannot divide by zero

---

**Multiple catch Blocks -**

Multiple `catch` blocks can be used to handle different exceptions.

Example:

class MultipleCatchExample
{
    public static void main(String[] args)
    {
        try
        {
            int[] arr = {1, 2, 3};
            System.out.println(arr[5]);
        }
        catch (ArithmeticException e)
        {
            System.out.println("Arithmetic exception occurred");
        }
        catch (ArrayIndexOutOfBoundsException e)
        {
            System.out.println("Array index out of bounds");
        }
    }
}

---

**finally Block -**

The `finally` block executes **whether an exception occurs or not**. It is commonly used for cleanup operations.

Example:

class FinallyExample
{
    public static void main(String[] args)
    {
        try
        {
            int x = 10 / 2;
            System.out.println(x);
        }
        catch (Exception e)
        {
            System.out.println("Exception occurred");
        }
        finally
        {
            System.out.println("Execution completed");
        }
    }
}

**Output:**

5  
Execution completed

---

**throw Keyword -**

The `throw` keyword is used to **explicitly throw an exception**.

Example:

class ThrowExample
{
    public static void main(String[] args)
    {
        int age = 15;
        if (age < 18)
        {
            throw new ArithmeticException("Not eligible to vote");
        }
    }
}

---

**throws Keyword -**

The `throws` keyword is used to *declare exceptions* that may be thrown by a method.

Example:

class ThrowsExample
{
    static void check() throws Exception
    {
        throw new Exception("Exception thrown");
    }

    public static void main(String[] args)
    {
        try
        {
            check();
        }
        catch (Exception e)
        {
            System.out.println(e.getMessage());
        }
    }
}

---

**Important Points to Remember -**

• Exceptions are runtime errors  
• `try` block contains risky code  
• `catch` block handles exceptions  
• `finally` always executes  
• `throw` explicitly throws an exception  
• `throws` declares exceptions  

---

**Exception Hierarchy (Simplified) -**

• Object  
  • Throwable  
    • Exception  
      • RuntimeException  
    • Error  

---

**Summary:**

• Exception handling prevents abnormal termination  
• Java supports checked and unchecked exceptions  
• `try-catch-finally` handles runtime errors  
• `throw` and `throws` control exception flow  
• Exception handling improves program safety and reliability
