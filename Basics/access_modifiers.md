
**Definition:**

**Access modifiers** in Java are keywords used to control the visibility and accessibility of classes, methods,
constructors and variables. They define *where* a member can be accessed from and help in implementing security and
encapsulation in programs.

---

**Types of Access Modifiers in Java:**

Java provides four types of access modifiers:

1. public  
2. protected  
3. default (no keyword)  
4. private  

---

**1. public Access Modifier -**

The `public` access modifier makes a class or member accessible **from anywhere** in the program.

Example:

class PublicExample
{
    public int number = 10;

    public void show()
    {
        System.out.println("Public method");
    }
}

**Explanation:**

• Accessible within the same class  
• Accessible within the same package  
• Accessible outside the package  
• Accessible by subclasses  

---

**2. private Access Modifier -**

The `private` access modifier restricts access **only to the same class**.

Example:

class PrivateExample
{
    private int value = 5;

    private void display()
    {
        System.out.println("Private method");
    }
}

**Explanation:**

• Accessible only within the same class  
• Not accessible outside the class  
• Commonly used for data hiding  

---

**3. default Access Modifier (No Keyword) -**

When no access modifier is specified, Java applies the **default** access level. It allows access **only within the same
package**.

Example:

class DefaultExample
{
    int data = 20;

    void show()
    {
        System.out.println("Default access");
    }
}

**Explanation:**

• Accessible within the same class  
• Accessible within the same package  
• Not accessible outside the package  

---

**4. protected Access Modifier -**

The `protected` access modifier allows access **within the same package** and **in subclasses** outside the package.

Example:

class ProtectedExample
{
    protected int marks = 80;

    protected void display()
    {
        System.out.println("Protected access");
    }
}

**Explanation:**

• Accessible within the same class  
• Accessible within the same package  
• Accessible in subclasses  
• Not accessible through normal objects outside the package  

---

**Comparison of Access Modifiers -**

| Access Level | Same Class | Same Package | Subclass | Outside Package |
|-------------|------------|--------------|----------|-----------------|
| public      | Yes        | Yes          | Yes      | Yes             |
| protected   | Yes        | Yes          | Yes      | No              |
| default     | Yes        | Yes          | No       | No              |
| private     | Yes        | No           | No       | No              |

---

**Important Points to Remember -**

• Access modifiers improve security  
• `private` is the most restrictive  
• `public` is the least restrictive  
• Only one public class is allowed per file  
• Access modifiers help control data access  

---

**Summary:**

• Access modifiers define the visibility of class members  
• Java provides four access levels  
• They help in data hiding and security  
• Proper use makes code safer and more maintainable
