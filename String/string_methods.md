
**Definition:**

Java provides many **built-in methods** in the `String` class to perform operations such as finding length, accessing
characters, comparing strings, extracting parts of strings and modifying string values.

These methods are widely used in real programs and interview problems.

---

**1. length() -**

Returns the number of characters in a string.

Example:

class LengthExample
{
    public static void main(String[] args)
    {
        String s = "Java";
        System.out.println(s.length());
    }
}

**Output:**

4

---

**2. charAt() -**

Returns the character at a specified index.

Example:

class CharAtExample
{
    public static void main(String[] args)
    {
        String s = "Java";
        System.out.println(s.charAt(1));
    }
}

**Output:**

a

---

**3. substring() -**

Extracts a part of the string.

Example:

class SubstringExample
{
    public static void main(String[] args)
    {
        String s = "Programming";
        System.out.println(s.substring(0, 7));
    }
}

**Output:**

Program

---

**4. equals() -**

Compares the content of two strings.

Example:

class EqualsExample
{
    public static void main(String[] args)
    {
        String a = "Java";
        String b = "Java";

        System.out.println(a.equals(b));
    }
}

**Output:**

true

---

**5. equalsIgnoreCase() -**

Compares strings ignoring case.

Example:

class EqualsIgnoreCaseExample
{
    public static void main(String[] args)
    {
        String a = "Java";
        String b = "java";

        System.out.println(a.equalsIgnoreCase(b));
    }
}

**Output:**

true

---

**6. compareTo() -**

Compares two strings lexicographically.

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

---

**7. toUpperCase() and toLowerCase() -**

Converts string to upper or lower case.

Example:

class CaseConversionExample
{
    public static void main(String[] args)
    {
        String s = "Java";

        System.out.println(s.toUpperCase());
        System.out.println(s.toLowerCase());
    }
}

**Output:**

JAVA  
java  

---

**8. trim() -**

Removes extra spaces from the beginning and end.

Example:

class TrimExample
{
    public static void main(String[] args)
    {
        String s = "  Java  ";
        System.out.println(s.trim());
    }
}

**Output:**

Java

---

**9. replace() -**

Replaces characters or substrings.

Example:

class ReplaceExample
{
    public static void main(String[] args)
    {
        String s = "Java";
        System.out.println(s.replace('a', 'o'));
    }
}

**Output:**

`Jovo`

---

**10. contains() -**

Checks whether a string contains a specific sequence.

Example:

class ContainsExample
{
    public static void main(String[] args)
    {
        String s = "Java Programming";
        System.out.println(s.contains("Java"));
    }
}

**Output:**

true

---

**Important Points to Remember -**

• String methods do not modify the original string  
• Most methods return a new string  
• Indexing starts from 0  
• String comparison should use `equals()` not `==`  

---

**Summary:**

• Java provides many useful string methods  
• Methods help manipulate and analyze strings  
• Strings remain immutable after method calls  
• String methods are essential for problem solving
