
**Definition:**

In Java, a **String is immutable**, which means once a String object is created, its value cannot be changed. Any
operation that appears to modify a string actually creates a `new String object` in memory.

---

**What Does Immutability Mean?**

Immutability means:

• The content of a String cannot be modified  
• Changes result in a new object  
• The original String remains unchanged  

---

**Example of String Immutability -**

Example:

class StringImmutabilityExample
{
    public static void main(String[] args)
    {
        String s = "Java";
        s.concat(" Programming");

        System.out.println(s);
    }
}

**Output:**

Java

Even though `concat()` was used, the original string `s` did not change.

---

**Why Did the String Not Change?**

• `concat()` creates a new String object  
• The new value was not assigned to any variable  
• The original String remains unchanged  

Correct way:

String s = "Java";
s = s.concat(" Programming");

System.out.println(s);

**Output:**

Java Programming

---

**Memory Explanation (String Pool) -**

• String literals are stored in the 'String Constant Pool'  
• Reusing strings saves memory  
• Immutability helps improve security and performance  

---

**Why Strings Are Immutable in Java -**

• Improves security  
• Enables String pooling  
• Makes strings thread-safe  
• Prevents accidental modification  

---

**Comparison with StringBuilder -**

Example:

class StringBuilderExample
{
    public static void main(String[] args)
    {
        StringBuilder sb = new StringBuilder("Java");
        sb.append(" Programming");

        System.out.println(sb);
    }
}

**Output:**

Java Programming

Here, the value changes because `StringBuilder` is **mutable**.

---

**Important Points to Remember -**

• String objects cannot be modified  
• All string operations create new objects  
• `StringBuilder` and `StringBuffer` are mutable  
• Immutability improves safety and efficiency  

---

**Summary:**

• Strings in Java are immutable  
• Any modification creates a new object  
• Original string remains unchanged  
• Immutability is a key feature of Java strings
