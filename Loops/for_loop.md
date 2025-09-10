
For Loop in Java

● Definition :
The for loop in Java is a control structure that allows you to execute a block of code a fixed number of times. It is most commonly used when the number of iterations is known in advance.

● Syntax :
for(initialization; condition; update)
{
  // loop body
}

● Explanation of Parts :

● Initialization → Runs once at the beginning; usually used to declare and set a loop variable.

● Condition → Checked before each iteration. If true, the loop executes; if false, the loop ends.

● Update → Executed after each iteration, generally used to modify the loop variable (e.g., increment or decrement).

{
 public static void main(String[] args)
 {
  // Print numbers from 1 to 5
  for(int i = 1; i <= 5; i++)
  {
   System.out.println("Number: " + i);
  }
 }
}

● Output :
Number: 1
Number: 2
Number: 3
Number: 4
Number: 5

● Key Notes :

● Initialization, condition, and update are optional (but semicolons are mandatory).

● Infinite loop is possible using for(;;) if no condition is provided.

● Multiple variables can be initialized or updated in a single for loop.
