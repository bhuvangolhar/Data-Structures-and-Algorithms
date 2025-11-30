....
**Definition:**

In Java, a **String** is one of the most commonly used and most powerful data types. It is a `sequence of characters` 
enclosed within double quotes (" ") and is used to store and manipulate text data such as words, sentences, or symbols.
Unlike many other programming languages where strings are just arrays of characters, in Java, a *String is an object* 
of the `java.lang.String` class, which provides numerous built-in methods for performing operations like concatenation,
comparison, searching, and modification. A String in Java is an object that represents a sequence of characters. 
It is *immutable*, meaning once a string object is created, its value *cannot be changed*.

**Declaration and Initialization of Strings:**

Strings can be created in two main ways which are as follows,

1. **Using String Literal -**

   String str1 = "Hello";

   – Stored in the String Constant Pool (a special memory area inside the heap).
   – If another string with the same value already exists in the pool, Java does not create a new object,
     it reuses the existing one (saves memory).

2. **Using `new` Keyword -**

   String str2 = new String("Hello");

   – Always creates a new String object in the heap memory, even if the same string exists in the pool.

**Example:**

class Example 
{
    public static void main(String[] args) 
    {
        String s1 = "Java";
        String s2 = "Java";
        String s3 = new String("Java");
        System.out.println(s1 == s2); // true - same reference in pool
        System.out.println(s1 == s3); // false - different object in heap
    }
}

**Output:**

true
false

**Explanation:**

– `s1` and `s2` share the same reference in the String Constant Pool.
– `s3` is created separately in the heap memory, so it has a different reference.

**Immutability of Strings:**

Once a String object is created, it cannot be changed.
Any operation that seems to modify a string actually creates a new String object.

**Example:**

class Example 
{
    public static void main(String[] args) 
    {
        String s = "Hello";
        s.concat(" World");
        System.out.println(s);  // Output: Hello
    }
}

**Explanation:**

– The method `concat()` creates a new string `"Hello World"` but does not change the original `"Hello"`.
– Since `s` is immutable, to update it, you must assign the result to `s` again:

  s = s.concat(" World");

**Commonly Used String Methods:**

| **Method**                      | **Description**                  | **Example / Output**                       |
| ------------------------------- | -------------------------------- | ------------------------------------------ |
| `length()`                      | Returns length of string         | `"Java".length()` → `4`                    |
| `charAt(int index)`             | Returns character at given index | `"Java".charAt(2)` → `'v'`                 |
| `toUpperCase()`                 | Converts to uppercase            | `"java".toUpperCase()` → `"JAVA"`          |
| `toLowerCase()`                 | Converts to lowercase            | `"JAVA".toLowerCase()` → `"java"`          |
| `concat(String s)`              | Joins two strings                | `"Hello".concat("World")` → `"HelloWorld"` |
| `equals(String s)`              | Compares contents                | `"Java".equals("java")` → `false`          |
| `equalsIgnoreCase(String s)`    | Compares ignoring case           | `"Java".equalsIgnoreCase("java")` → `true` |
| `substring(int start, int end)` | Returns part of string           | `"Programming".substring(0,4)` → `"Prog"`  |
| `contains(String s)`            | Checks if substring exists       | `"Hello".contains("ell")` → `true`         |
| `replace(char old, char new)`   | Replaces characters              | `"Java".replace('a','o')` → `"Jovo"`       |
| `trim()`                        | Removes extra spaces             | `" Hello ".trim()` → `"Hello"`             |

**String Concatenation:**

You can join two or more strings using:

1. The `+` operator

   String name = "Java" + " Programming";

2. The `concat()` method

   String result = "Java".concat(" Rocks");

Both produce:

Java Programming
Java Rocks

**String Comparison:**

There are two ways to compare strings -

i)  Using `==` → compares memory references (not content).
ii) Using `.equals()` → compares actual string content.

**Example:**

String s1 = "Hello";
String s2 = "Hello";
String s3 = new String("Hello");
System.out.println(s1 == s2);      // true (same reference)
System.out.println(s1 == s3);      // false (different objects)
System.out.println(s1.equals(s3)); // true (same content)

**Why Strings are Immutable in Java:**

1. **Security -** Prevents malicious modification of data like database URLs or file paths.
2. **String Pool Efficiency -** Allows reusing existing strings in the pool, saving memory.
3. **Thread Safety -** Immutable strings can be safely shared between threads.
4. **Caching -** Since values don’t change, hash codes of strings can be cached for faster operations.

**StringBuffer & StringBuilder (Briefly):**

– **StringBuffer -** Mutable version of String, thread-safe (synchronized).
– **StringBuilder -** Mutable version of String, not thread-safe but faster.
  (Both allow modification of string content without creating new objects — we’ll discuss them in detail later.)

**Real-Life Analogy:**

Think of a **String** as a sealed envelope — once you write something inside and seal it, you can’t change what’s written; you can only create a new envelope with the updated message.

**Key Points:**

– String is a class in `java.lang` package.
– Strings are immutable and stored in the String Constant Pool.
– Common operations include concatenation, comparison, searching, and case conversion.
– Use `StringBuffer` or `StringBuilder` for mutable string operations.

**In Summary:**

A **String** in Java is an immutable object used to represent a sequence of characters.
It provides rich functionality for text manipulation while ensuring security, efficiency, 
and consistency 
in memory handling.
.
