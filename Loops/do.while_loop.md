
**Definition:**

The **`do-while` loop** in Java is a variation of the `while` loop that ensures the loop body executes at least once, 
regardless of the condition. This is because, unlike other loops, the condition is evaluated after the execution of the 
loop body. It is particularly useful when you want to *perform an action first* and then decide whether to repeat it 
based on a certain condition — for example, taking user input repeatedly until they choose to exit.

**Syntax:**

do 
{
    // Code to be executed
} 
while (condition);

**Note:** The semicolon (`;`) at the end of the `while` statement is mandatory in a `do-while` loop.

**Explanation of Components:**

a) **Loop Body:**

   ‣ Contains the statements that need to be executed repeatedly.
   
   ‣ This block executes **at least once**, even if the condition is false initially.

b) **Condition:**

   ‣ A **boolean expression** evaluated **after** the execution of the loop body.
   
   ‣ If the condition is **true**, the loop executes again.
   
   ‣ If the condition is **false**, the loop stops, and control moves to the next statement after the loop.

**Flow of Execution:**

1. The program *enters the loop body* and executes it *once*, without checking the condition initially.
   
2. After executing the body, the *condition is evaluated*.
   
3. If the condition is *true*, the loop body executes again.
   
4. This process repeats until the condition becomes *false*.
   
5. When the condition is false, control moves to the statement following the loop.

**Example:**

class Example 
{
    public static void main(String[] args) 
    {
        int i = 1;
        do {
            System.out.println("Count: " + i);
            i++;
           } 
        while(i <= 5);
    }
}

**Output:**

Count: 1

Count: 2

Count: 3

Count: 4

Count: 5

**Key Points:**

‣ The *`do-while` loop guarantees one execution* of the loop body, even if the condition is false initially.

‣ Commonly used in *menu-driven programs* or *user-interactive applications*, where at least one iteration is required.

‣ Make sure the loop has a *condition that can eventually become false*; otherwise, it may lead to an *infinite loop*.

‣ Syntax-wise, it’s the only loop in Java that ends with a *semicolon (`;`)* after the condition.
