Operators in Java

Operators in Java are special symbols used to perform operations on variables and values.
They are the **building blocks of logic** in every Java program.

 Types of Operators

 1. **Arithmetic Operators**

Used to perform basic mathematical operations.

| Operator | Description         | Example |
| -------- | ------------------- | ------- |
| `+`      | Addition            | `a + b` |
| `-`      | Subtraction         | `a - b` |
| `*`      | Multiplication      | `a * b` |
| `/`      | Division            | `a / b` |
| `%`      | Modulus (remainder) | `a % b` |

**Example in Java:**

class ArithmeticExample {
    public static void main(String[] args) {
        int a = 10, b = 3;
        System.out.println("a + b = " + (a + b));
        System.out.println("a - b = " + (a - b));
        System.out.println("a * b = " + (a * b));
        System.out.println("a / b = " + (a / b));
        System.out.println("a % b = " + (a % b));
    }
}

 2. **Relational Operators**

Used to compare two values, returning `true` or `false`.

| Operator | Description              | Example  |
| -------- | ------------------------ | -------- |
| `==`     | Equal to                 | `a == b` |
| `!=`     | Not equal to             | `a != b` |

 3. **Logical Operators**

Used to combine multiple conditions.

| Operator | Description | Example             |            |          |   |           |
| -------- | ----------- | ------------------- | ---------- | -------- | - | --------- |
| `&&`     | Logical AND | `(a > 5 && b < 10)` |            |          |   |           |
| \`       |             | \`                  | Logical OR | \`(a > 5 |   | b < 10)\` |
| `!`      | Logical NOT | `!(a > b)`          |            |          |   |           |

 4. **Assignment Operators**

Used to assign values to variables.

| Operator | Example  | Equivalent       |
| -------- | -------- | ---------------- |
| `=`      | `a = 5`  | Assigns 5 to `a` |
| `+=`     | `a += 3` | `a = a + 3`      |



 5. **Unary Operators**

Work on a single operand.

| Operator | Description            | Example        |
| -------- | ---------------------- | -------------- |
| `++`     | Increment by 1         | `a++` or `++a` |
| `--`     | Decrement by 1         | `a--` or `--a` |
| `+`      | Unary plus (no effect) | `+a`           |
| `-`      | Unary minus (negation) | `-a`           |

 6. **Ternary Operator (`?:`)**

A shorthand for `if-else`.

int age = 20;
String result = (age >= 18) ? "Adult" : "Minor";
System.out.println(result); // Adult

 7. **Bitwise Operators**

Operate at the binary level.

| Operator | Description          | Example    |     |     |
| -------- | -------------------- | ---------- | --- | --- |
| `&`      | Bitwise AND          | `a & b`    |     |     |
| \`       | \`                   | Bitwise OR | \`a | b\` |
| `^`      | Bitwise XOR          | `a ^ b`    |     |     |
| `~`      | Bitwise NOT          | `~a`       |     |     |
| `<<`     | Left shift           | `a << 2`   |     |     |
| `>>`     | Right shift         
 Why are Operators Important?

* They help in **decision-making** (logical & relational).
* Perform **calculations** in algorithms.
* Used in **loops, conditions, and data manipulation**.
* Essential for writing **expressive, optimized code**.


