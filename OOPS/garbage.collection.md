
**Important Note:**

Java does not support destructors like C or C++. Instead, Java uses an automatic process called **garbage collection**
to manage memory and destroy unused objects.

---

**What is Garbage Collection?**

-> Garbage collection in Java is the process of automatically removing unused objects from memory. It helps free memory
by destroying objects that are no longer referenced in the program.

The garbage collector runs automatically and is managed by the **Java Virtual Machine (`JVM`)**.

---

**Why Java Does Not Have Destructors:**

• Java manages memory automatically  
• Manual destruction can cause errors  
• Garbage collection improves safety  
• Developers do not need to free memory explicitly  

---

**When Does an Object Become Eligible for Garbage Collection?**

An object becomes eligible for garbage collection when:

• It is no longer referenced by any variable  
• The reference is set to `null`  
• The object goes out of scope  

Example:

class GarbageExample
{
    public static void main(String[] args)
    {
        GarbageExample obj = new GarbageExample();
        obj = null;   // object eligible for garbage collection
    }
}

---

**The finalize() Method (Destructor-like Behavior) -**

The `finalize()` method is a method that is called by the garbage collector **before destroying an object**. It can be
used to perform cleanup operations.

Example:

class FinalizeExample
{
    protected void finalize()
    {
        System.out.println("Object is destroyed");
    }

    public static void main(String[] args)
    {
        FinalizeExample obj = new FinalizeExample();
        obj = null;
        System.gc();   // request garbage collection
    }
}

**Output:**

Object is destroyed

---

**Important Points About finalize() -**

• `finalize()` is not guaranteed to run  
• It is called automatically by the JVM  
• Programmers should not rely on it  
• It is deprecated in modern Java versions  

---

**Better Alternative to finalize():**

Java recommends using:

• try-with-resources  
• Explicit close methods  
• Proper resource management  

Example:

try (FileInputStream file = new FileInputStream("data.txt"))
{
    // use file
}

---

**Destructor vs Garbage Collection -**

| Feature        | Destructor (C++)      | Garbage Collection (Java) |
|---------------|-----------------------|---------------------------|
| Memory control| Manual                | Automatic                 |
| Destructor    | Yes                   | No                        |
| Cleanup timing| Predictable           | Not predictable           |
| Safety        | Less safe             | More safe                 |

---

**Summary:**

• Java does not have destructors  
• Memory is managed using garbage collection  
• `finalize()` provides destructor-like behavior  
• Garbage collection is automatic and JVM-controlled  
• Proper resource management is preferred
