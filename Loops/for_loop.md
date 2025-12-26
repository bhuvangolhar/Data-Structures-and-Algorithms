
**Definition:**

The **`for` loop** in Java is one of the most commonly used looping structures. It is primarily used when the *number of 
iterations* is known in advance — for example, when you need to execute a block of code a specific number of times or iterate
through a range of numbers. The `for` loop provides a compact and clear syntax because all the essential loop-control
elements (initialization, condition, and update) are written together in a single line, making it easy to read and manage.

**Syntax:**

for(initialization; condition; update) 
{
    // Code to be executed
}

**Explanation of Components:**

a) **Initialization:**
   
   This step runs *only once* at the beginning of the loop. It is usually used to declare and initialize
   a loop control variable.
   
   Example: `int i = 0;`

b) **Condition:**
   
   Before each iteration, the condition is *evaluated*.

   • If the condition is *true*, the loop body executes.
  
   • If it becomes *false*, the loop terminates, and control moves to the next statement after the loop.
     Example: `i < 5;`

c) **Update (Iteration Expression):**

   This part runs *after each iteration* of the loop body. It’s commonly used to modify the loop
   control variable (like incrementing or decrementing it).
   
   Example: `i++`

**Flow of Execution:**

1. The *initialization* executes once.
2. The *condition* is checked — if true, the loop body executes.
3. After the body executes, the *update* expression runs.
4. The condition is checked again, and the process repeats until the condition becomes false.

**Example:**

class Example 
{
    public static void main(String[] args) 
    {
        for(int i = 1; i <= 5; i++) 
        {
            System.out.println("Count: " + i);
        }
    }
}

**Output:**

Count: 1
Count: 2
Count: 3
Count: 4
Count: 5

**Key Points:**

• The `for` loop is best suited when the *number of iterations* is predetermined.

• You can declare multiple variables in the initialization part (e.g., `for(int i = 0, j = 10; i < j; i++, j--)`).
  
• The condition and update expressions can be omitted, but the semicolons must remain 
  (e.g., `for(;;)` creates an `infinite loop`).
  
• It offers better readability and control when compared to other loops for fixed iteration tasks.
