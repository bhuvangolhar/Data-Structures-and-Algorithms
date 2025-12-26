
**Definition:**

The **`while` loop** in Java is a control flow statement that allows code to be executed *repeatedly* based on a given 
boolean condition. It is mainly used when the number of iterations is not known in advance, and the loop needs to continue 
running until a certain condition becomes false. Unlike the `for` loop, where initialization, condition, and update are 
written together, the `while` loop keeps them separate, offering greater flexibility for cases where the loop control 
variable or condition may change inside the loop body.

**Syntax:**

while(condition) 
{
    // Code to be executed repeatedly
}

**Explanation of Components:**

1. **Condition -**

   ▪ The condition is a `boolean expression` that is checked before each iteration.
   ▪ If the condition evaluates to `true`, the loop body executes.
   ▪ If it evaluates to `false`, the loop stops, and control moves to the next statement after the loop.

2. **Loop Body -**

   ▪ Contains the code that needs to be executed repeatedly as long as the condition remains true.
   ▪ It usually includes statements that modify variables involved in the condition to eventually end the loop.

**Flow of Execution:**

1) The condition is checked first.
   
2) If the condition is true, the loop body executes.
   
3) After executing the loop body, the program goes back to check the condition again.
   
4) This process continues until the condition becomes false.
   
5) Once the condition is false, the loop terminates and control moves to the next line after the loop.

**Example:**

class Example 
{
    public static void main(String[] args) 
    {
        int i = 1;
        while(i <= 5) 
        {
            System.out.println("Count: " + i);
            i++;  // Incrementing to eventually end the loop
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

▪ The condition is tested first, so if it is false initially, the loop body may not execute even once.
  
▪ Best used when the *number of repetitions* is uncertain and depends on a dynamic condition.
  
▪ It’s crucial to ensure that something in the loop body changes the condition, otherwise it can lead to
  an *infinite loop*.
  
▪ The initialization and update expressions are usually written outside the loop (unlike in a `for` loop).
