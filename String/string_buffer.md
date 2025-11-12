
**Definition:**

In Java, the **`StringBuffer`** class is a **mutable sequence of characters**, just like `StringBuilder`. It allows you 
to **modify strings (append, insert, delete, reverse, etc.)** without creating new objects each time a change is made.
The key difference between `StringBuffer` and `StringBuilder` is that **`StringBuffer` is synchronized (thread-safe)**, 
meaning it can be safely used in **multi-threaded environments**, where multiple threads access the same string object 
simultaneously. StringBuffer in Java is a **thread-safe, mutable class** used to create and manipulate dynamic strings.
It ensures that **only one thread can modify the string at a time**, maintaining data consistency in concurrent situations.

**Key Features:**

1. **Mutable:** You can modify its content without creating new objects.
2. **Thread-safe:** All methods are synchronized, meaning safe for use by multiple threads.
3. **Slower than `StringBuilder`:** Due to synchronization overhead.
4. **Stored in Heap Memory:** Unlike string literals, which are stored in the String Constant Pool.

**Syntax:**

StringBuffer sb = new StringBuffer();              // Empty buffer
StringBuffer sb2 = new StringBuffer("Hello");      // Initialized with text

**Example:**

class Example {
    public static void main(String[] args) {
        StringBuffer sb = new StringBuffer("Java");
        sb.append(" Programming");   // Add text
        System.out.println(sb);      // Output: Java Programming
        sb.insert(5, "Language ");   // Insert at index
        System.out.println(sb);      // Output: Java Language Programming
        sb.replace(5, 13, "Code");   // Replace text
        System.out.println(sb);      // Output: Java Code Programming
        sb.delete(5, 10);            // Delete characters
        System.out.println(sb);      // Output: Java Programming
        sb.reverse();                // Reverse string
        System.out.println(sb);      // Output: gnimmargorP avaJ
    }
}

**Commonly Used Methods of StringBuffer:**

| **Method**                              | **Description**                 | **Example / Output**                     |
| --------------------------------------- | ------------------------------- | ---------------------------------------- |
| `append(String s)`                      | Adds text to the end            | `"Hello".append(" Java") → "Hello Java"` |
| `insert(int index, String s)`           | Inserts text at specific index  | `"Java".insert(4,"X") → "JavaX"`         |
| `replace(int start, int end, String s)` | Replaces text between indexes   | `"Java".replace(1,3,"XX") → "JXXa"`      |
| `delete(int start, int end)`            | Deletes part of text            | `"Hello".delete(1,3) → "Ho"`             |
| `reverse()`                             | Reverses entire string          | `"Java".reverse() → "avaJ"`              |
| `capacity()`                            | Returns current buffer size     | Default: 16 + string length              |
| `length()`                              | Returns current string length   | `"Hello".length() → 5`                   |
| `toString()`                            | Converts StringBuffer to String | `sb.toString()`                          |

**Immutability vs. Mutability Example:**

class Example {
    public static void main(String[] args) {
        String s = "Hello";
        s.concat(" World");
        System.out.println(s);  // Output: Hello (String is immutable)
        StringBuffer sb = new StringBuffer("Hello");
        sb.append(" World");
        System.out.println(sb); // Output: Hello World (StringBuffer is mutable)
    }
}

**StringBuffer vs StringBuilder vs String:**

| **Feature**           | **String**      | **StringBuffer**        | **StringBuilder**        |
| --------------------- | --------------- | ----------------------- | ------------------------ |
| **Mutability**        | Immutable       | Mutable                 | Mutable                  |
| **Thread-Safe**       | Yes             | Yes (synchronized)      | No                       |
| **Speed**             | Slow            | Moderate                | Fast                     |
| **Memory Efficiency** | Low             | High                    | High                     |
| **Best Used For**     | Fixed text data | Multi-threaded programs | Single-threaded programs |

**Thread Safety Example:**

class SafeExample {
    public static void main(String[] args) {
        StringBuffer shared = new StringBuffer("Start ");
        Thread t1 = new Thread(() -> {
            for (int i = 0; i < 3; i++)
                shared.append("A ");
        });
        Thread t2 = new Thread(() -> {
            for (int i = 0; i < 3; i++)
                shared.append("B ");
        });
        t1.start();
        t2.start();
        try { t1.join(); t2.join(); } catch (Exception e) {}
        System.out.println(shared);
    }
}

**Output (Example):**

Start A A A B B B

**Explanation:**

* `StringBuffer` ensures **synchronized access**, preventing data corruption when multiple threads modify the same object.
* Using `StringBuilder` here could lead to **inconsistent or jumbled output**.

**Advantages of StringBuffer:**

1. **Thread Safety:** Safe in multithreaded environments.
2. **Efficient Modifications:** No new object creation on change.
3. **Flexible Operations:** Supports append, delete, insert, reverse, and replace.
4. **Better Performance than String** for repeated modifications.

**Disadvantages:**

1. **Slower than StringBuilder** due to synchronization overhead.
2. **More memory usage** if thread safety is not required (unnecessary locking).

**Real-Life Analogy:**

Think of `StringBuffer` as a **shared notepad** — multiple people (threads) can write on it, but only **one person can write at a time**, ensuring the content stays safe and orderly.

**Key Points:**

* `StringBuffer` is **mutable** and **thread-safe**.
* Belongs to **`java.lang`** package.
* Offers synchronized methods for **safe concurrent use**.
* Use **`toString()`** to convert to a `String` when needed.
* Best for **multi-threaded programs** that modify strings frequently.

**In Summary:**

**`StringBuffer`** in Java is a **mutable, thread-safe** alternative to `String`.
It allows efficient string manipulation in **multi-threaded environments**, ensuring data consistency and reliability — 
though it’s slightly slower than `StringBuilder` due to synchronization.
