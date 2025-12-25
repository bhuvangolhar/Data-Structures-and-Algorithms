
**Definition:**

An **operator** in Java is a special symbol that performs a specific operation on one, two, or three operands (values or 
variables) and produces a result. Operators are used to perform different kinds of computations, such as arithmetic 
calculations, comparisons, logical decisions, and more. They are a fundamental part of any Java program because they help
manipulate data and control the flow of execution.

**Types of Operators:**

Java provides several types of operators that can be grouped based on the kind of operation they perform. 
The main categories are:

1. Arithmetic Operators  
2. Relational Operators  
3. Logical Operators  
4. Assignment Operators  
5. Unary Operators  
6. Bitwise Operators  
7. Ternary (Conditional) Operator  
8. Miscellaneous Operators  

Let’s look at each in detail,

**1. Arithmetic Operators -**

Arithmetic operators are used to perform basic mathematical operations like addition, subtraction, multiplication, division, and modulus (remainder).

Example:

• int a = 10, b = 3;  
• System.out.println(a + b);      // 13  
• System.out.println(a - b);     // 7  
• System.out.println(a * b);    // 30  
• System.out.println(a / b);   // 3  
• System.out.println(a % b);  // 1  

**Explanation:**

• `+` → Addition  
• `-` → Subtraction  
• `*` → Multiplication  
• `/` → Division (quotient)  
• `%` → Modulus (remainder)  

**2. Relational Operators -**

Relational operators are used to compare two values and return a boolean result (`true` or `false`).

Example:

• int x = 5, y = 10;  
• System.out.println(x == y);       // false  
• System.out.println(x != y);      // true  
• System.out.println(x > y);      // false  
• System.out.println(x < y);     // true  
• System.out.println(x >= y);   // false  
• System.out.println(x <= y);  // true  

**Explanation:**

They are used in conditions and loops to control program flow based on comparisons.

**3. Logical Operators -**

Logical operators are used to combine two or more conditions and return a boolean result.

Example:

• int a = 5, b = 10, c = 15;  
• System.out.println(a < b && b < c);   // true (both true)  
• System.out.println(a < b || b > c);  // true (one true)  
• System.out.println(!(a < b));       // false (reverses true)  

**Explanation:**

• `&&` → Logical AND (true if both are true)  
• `||` → Logical OR (true if any one is true)  
• `!` → Logical NOT (reverses the result)  

**4. Assignment Operators -**

Assignment operators are used to assign values to variables. The basic one is `=`, and there are also shorthand forms for combined operations.

Example:

• int a = 10;  
• a += 5;  // a = a + 5 → 15  
• a -= 3;  // a = a - 3 → 12  
• a *= 2;  // a = a * 2 → 24  
• a /= 4;  // a = a / 4 → 6  
• a %= 2;  // a = a % 2 → 0  

**Explanation:**

These help shorten expressions like `a = a + 5` into `a += 5`.

**5. Unary Operators -**

Unary operators work on a single operand. They are used for incrementing, decrementing, negating, or checking logical conditions.

Example:

• int x = 5;  
• System.out.println(++x);    // 6 (pre-increment)  
• System.out.println(x--);   // 6 then decreases to 5 (post-decrement)  
• System.out.println(-x);   // -5 (negation)  
• boolean flag = false;  
• System.out.println(!flag); // true  

**Explanation:**

• `++` → Increment by 1  
• `--` → Decrement by 1  
• `-` → Negation  
• `!` → Logical NOT  

**6. Bitwise Operators -**

Bitwise operators work at the **bit level** (binary representation of numbers). They are used mostly in low-level programming, graphics, and performance-based tasks.

Example:

• int a = 5;    // 0101  
• int b = 3;   // 0011  
• System.out.println(a & b);       // 1  (AND)  
• System.out.println(a | b);      // 7  (OR)  
• System.out.println(a ^ b);     // 6  (XOR)  
• System.out.println(~a);       // -6 (NOT)  
• System.out.println(a << 1);  // 10 (Left Shift)  
• System.out.println(a >> 1); // 2  (Right Shift)  

**Explanation:**

• `&` → Bitwise AND  
• `|` → Bitwise OR  
• `^` → Bitwise XOR  
• `~` → Bitwise NOT  
• `<<` → Left shift (multiplies by 2)  
• `>>` → Right shift (divides by 2)  

**7. Ternary Operator OR Conditional Operator -**

The ternary operator is a shortcut for an `if-else` statement. It takes three operands.

Syntax:

condition ? value_if_true : value_if_false;

Example:

• int age = 20;  
• String result = (age >= 18) ? "Adult" : "Minor";  
• System.out.println(result);  // Adult  

**Explanation:**

If the condition is true, it returns the first value; otherwise, it returns the second.

**8. Miscellaneous Operators -**

Java also includes a few special-purpose operators:

**a) `instanceof` Operator** →  

Checks whether an object is an instance of a particular class or subclass.  
String s = "Java";  
System.out.println(s instanceof String);  // true  

**b) `new` Operator** →  

Used to create new objects in memory.  
Car c = new Car();

**c) `[]` Operator** →  

Used to access elements in an array.  
int[] arr = {10, 20, 30};  
System.out.println(arr[1]);  // 20  

**Summary Table of Operators:**

| Type          | Symbols               | Example                | Description               |
| ------------- | --------------------- | ---------------------- | ------------------------- |
| Arithmetic    | +, -, *, /, %         | `a + b`                | Basic math operations     |
| Relational    | ==, !=, >, <, >=, <=  | `a > b`                | Compare two values        |
| Logical       | &&, ||, !             | `a && b`               | Combine conditions        |
| Assignment    | =, +=, -=, *=, /=, %= | `a += 5`               | Assign or update values   |
| Unary         | ++, --, -, !          | `++a`                  | Work on one variable      |
| Bitwise       | &, |, ^, ~, <<, >>    | `a & b`                | Work on bits              |
| Ternary       | ?:                    | `(a>b)?x:y`            | Shortcut for if-else      |
| Miscellaneous | new, instanceof, []   | `obj instanceof Class` | Special-purpose operators |

**Importance of Operators:**

Operators are the building blocks of Java expressions. They make it possible to perform calculations, make decisions,
compare values, and control logic in programs. Without operators, writing meaningful Java code would be almost impossible.
