
**Definition:**

**String comparison** in Java is used to check whether two strings are equal, not equal or to determine their
lexicographical order. Java provides multiple ways to compare strings and choosing the correct one is very important.

---

**Why String Comparison Is Important:**

• Used in conditions and decision making  
• Commonly asked in interviews  
• Prevents logical bugs  
• Helps compare string content correctly  

---

**1. Using == Operator -**

The `==` operator compares **references**, not actual string content.

Example:

class EqualityOperatorExample
{
    public static void main(String[] args)
    {
        String a = "Java";
        String b = "Java";

        System.out.println(a == b);
    }
}

**Output:**

true

Here, both strings refer to the same object in the String Constant Pool.

---

**Problem with == Operator -**

Example:

class EqualityIssueExample
{
    public static void main(String[] args)
    {
        String a = new String("Java");
        String b = new String("Java");

        System.out.println(a == b);
    }
}

**Output:**

false

Even though values are the same, references are different.

---

**2. Using equals() Method -**

The `equals()` method compares the 'actual content' of strings.

Example:

class EqualsMethodExample
{
    public static void main(String[] args)
    {
        String a = new String("Java");
        String b = new String("Java");

        System.out.println(a.equals(b));
    }
}

**Output:**

true

This is the 'recommended way' to compare strings.

---

**3. Using equalsIgnoreCase() Method -**

Compares strings while ignoring case differences.

Example:

class EqualsIgnoreCaseExample
{
    public static void main(String[] args)
    {
        String a = "JAVA";
        String b = "java";

        System.out.println(a.equalsIgnoreCase(b));
    }
}

**Output:**

true

---

**4. Using compareTo() Method -**

Compares strings lexicographically.

Example:

class CompareToExample
{
    public static void main(String[] args)
    {
        String a = "Apple";
        String b = "Banana";

        System.out.println(a.compareTo(b));
    }
}

**Output:**

Negative value

**Meaning:**

• 0 → Strings are equal  
• Negative → First string is smaller  
• Positive → First string is greater  

---

**Comparison Summary -**

| Method              | Compares        | Recommended |
|---------------------|-----------------|-------------|
| ==                  | Reference       | No          |
| equals()            | Content         | Yes         |
| equalsIgnoreCase()  | Content (ignore case) | Yes |
| compareTo()         | Lexicographical | Yes         |

---

**Important Points to Remember -**

• Use `equals()` to compare string values  
• Avoid using `==` for content comparison  
• `compareTo()` is useful for sorting  
• Case sensitivity matters unless ignored  

---

**Summary:**

• Java provides multiple ways to compare strings  
• `equals()` checks actual content  
• `==` checks memory reference  
• Proper comparison avoids logical errors
