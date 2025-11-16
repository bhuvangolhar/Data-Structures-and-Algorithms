
**Definition:**

In Java, the **`StringBuilder`** class is a mutable (changeable) sequence of characters. Unlike the `String` class, 
which creates a new object every time its value changes, `StringBuilder` allows you to modify the same object without 
creating new ones in memory. It is part of the `java.lang` package and was introduced in *Java 5* as a faster, 
non-synchronized alternative to `StringBuffer`. StringBuilder in Java is a *mutable class* used to create and manipulate 
dynamic strings efficiently. It allows modifications such as append, insert, delete, and reverse without creating new string
objects each time a change is made.

**Key Features:**

1) **Mutable -** Contents can be changed after creation.
2) **Faster than String and StringBuffer** (when not used in multithreading).
3) **Not thread-safe -** It is not synchronized, meaning multiple threads can cause conflicts if they access the same object
   simultaneously.
4) **Stored in Heap Memory -** Unlike string literals stored in the String Constant Pool.

**Syntax:**

StringBuilder sb = new StringBuilder();          // empty builder
StringBuilder sb2 = new StringBuilder("Hello");  // initialized with value

**Example:**
``
class Example {
    public static void main(String[] args) {
        StringBuilder sb = new StringBuilder("Java");
        sb.append(" Programming");  // adds text at end
        System.out.println(sb);     // Output: Java Programming
        sb.insert(5, "Language ");  // inserts text at index 5
        System.out.println(sb);     // Output: Java Language Programming
        sb.replace(5, 13, "Code");  // replaces part of text
        System.out.println(sb);     // Output: Java Code Programming
        sb.delete(5, 10);           // deletes characters
        System.out.println(sb);     // Output: Java Programming
        sb.reverse();               // reverses the string
        System.out.println(sb);     // Output: gnimmargorP avaJ
    }
}
``
**Commonly Used Methods of StringBuilder:**

| **Method**                              | **Description**                         | **Example / Output**                   |
| --------------------------------------- | --------------------------------------- | -------------------------------------- |
| `append(String s)`                      | Adds text at the end                    | `"Java".append(" Code") → "Java Code"` |
| `insert(int index, String s)`           | Inserts text at specified index         | `"Java".insert(4, "X") → "JavaX"`      |
| `replace(int start, int end, String s)` | Replaces text between indexes           | `"Java".replace(1,3,"XX") → "JXXa"`    |
| `delete(int start, int end)`            | Deletes text between indexes            | `"Hello".delete(1,3) → "Ho"`           |
| `reverse()`                             | Reverses string content                 | `"Java".reverse() → "avaJ"`            |
| `capacity()`                            | Returns current buffer size             | default: 16 + string length            |
| `length()`                              | Returns current string length           | `"Java".length() → 4`                  |
| `toString()`                            | Converts StringBuilder to normal String | `sb.toString()`                        |

**Immutability vs. Mutability Example:**

class Example 
{
    public static void main(String[] args) 
    {
        String s = "Hello";
        s.concat(" World"); 
        System.out.println(s); // Output: Hello (immutable)
        StringBuilder sb = new StringBuilder("Hello");
        sb.append(" World");
        System.out.println(sb); // Output: Hello World (mutable)
    }
}

**Explanation:**

• `String` creates a **new object** when modified (original remains unchanged).
• `StringBuilder` **modifies the existing object** in memory — faster and more efficient.

**Performance Comparison:**

| Feature       | **String**                        | **StringBuilder**        |
| ------------- | --------------------------------- | ------------------------ |
| Mutability    | Immutable                         | Mutable                  |
| Memory Usage  | Creates new object on each change | Uses same object         |
| Thread-Safe   | Yes                               | No                       |
| Speed         | Slower                            | Faster                   |
| Best Used For | Fixed text                        | Frequently modified text |

**When to Use StringBuilder:**

• When you need to concatenate or modify strings repeatedly (e.g., building SQL queries, file content, or loops).
• When working in a single-threaded environment (since it’s not synchronized).
• When performance and memory efficiency are important.

**Real-Life Analogy:**

Think of a **String** as a **sealed letter** — once sealed, it cannot be edited; you must write a new one for every change.
`StringBuilder`, on the other hand, is like a **whiteboard** — you can **erase, rewrite, and update** freely without 
creating a new board every time.

**Key Points:**

• `StringBuilder` is **mutable** and part of `java.lang` package.
• It is **not synchronized** (hence not thread-safe).
• It offers **better performance** in non-concurrent environments.
• Provides methods for efficient string manipulation (`append`, `insert`, `delete`, `replace`, etc.).
• Use `toString()` to convert a `StringBuilder` object into a `String`.

**In Summary:**

`StringBuilder` in Java provides a **fast and memory-efficient** way to handle **dynamic string operations**.
It’s ideal for situations where strings are **frequently modified** — making programs **faster, cleaner, and more 
efficient** than those that rely solely on immutable `String` objects.
