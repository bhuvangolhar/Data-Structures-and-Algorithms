
**Definition:**

A **`package`** in Java is a *namespace* that groups related classes and interfaces together. Packages are used to organize
code, avoid name conflicts and make programs easier to maintain and understand.

Java provides `built-in` packages, and programmers can also create their own custom packages.

---

**Why Packages Are Used?**

• Organize large projects into logical groups  
• Avoid class name conflicts  
• Improve code reusability  
• Control access using access modifiers  
• Make code easier to maintain  

---

**Types of Packages in Java:**

Java packages are mainly of two types:

1. Built-in Packages  
2. User-defined Packages  

---

**1. Built-in Packages -**

Java provides many built-in packages that contain predefined classes and interfaces.

Common examples:

• `java.lang` → basic classes (String, Math, Integer)  
• `java.util` → utility classes (Scanner, ArrayList)  
• `java.io` → input/output classes  
• `java.time` → date and time classes  

Example:

import java.util.Scanner;

class BuiltInPackageExample
{
    public static void main(String[] args)
    {
        Scanner scan = new Scanner(System.in);
        System.out.println("Built-in package example");
    }
}

---

**2. User-defined Packages -**

Programmers can create their own packages to organize classes.

Syntax to create a package:

package packageName;

Example:

package mypackage;

public class MyClass
{
    public void show()
    {
        System.out.println("This is a user-defined package");
    }
}

---

**Accessing Classes from a Package -**

Classes inside a package can be accessed using the `import` keyword.

Example:

import mypackage.MyClass;

class PackageAccessExample
{
    public static void main(String[] args)
    {
        MyClass obj = new MyClass();
        obj.show();
    }
}

---

**Using import Statement -**

There are two ways to use `import`:

• Import a specific class  
  import java.util.Scanner;  

• Import all classes of a package  
  import java.util.*;  

---

**Important Points to Remember -**

• A package must be declared at the top of the source file  
• One package can contain multiple classes  
• Package name usually follows lowercase naming convention  
• `java.lang` package is imported automatically  
• Packages help in large-scale application development  

---

**Summary:**

• Packages group related classes together  
• Java provides built-in and user-defined packages  
• `import` keyword is used to access package classes  
• Packages improve code organization and readability
