
**Definition:**

A **nested loop** is a loop placed inside another loop. The inner loop executes completely for each iteration of the
*outer loop*. Nested loops are commonly used when working with tables, matrices, patterns and multi-level repetition.

---

**How Nested Loops Work -**

• The outer loop controls the number of times the inner loop runs  
• For each iteration of the outer loop, the inner loop starts from the beginning  
• Execution continues until all iterations are completed  

---

**1. Basic Nested for Loop Example -**

Example:

class NestedForLoopExample
{
    public static void main(String[] args)
    {
        for (int i = 1; i <= 3; i++)
        {
            for (int j = 1; j <= 3; j++)
            {
                System.out.print(j + " ");
            }
            System.out.println();
        }
    }
}

**Output:**

1 2 3  
1 2 3  
1 2 3  

Here, the outer loop runs 3 times and the inner loop runs 3 times for each outer iteration.

---

**2. Nested Loop Using Different Variables -**

Example:

class NestedLoopExample
{
    public static void main(String[] args)
    {
        for (int i = 1; i <= 3; i++)
        {
            for (int j = 1; j <= i; j++)
            {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}

**Output:**

*  
* *  
* * *  

This example demonstrates how nested loops are used in pattern creation.

---

**3. Nested while Loop Example -**

Example:

class NestedWhileExample
{
    public static void main(String[] args)
    {
        int i = 1;
        while (i <= 3)
        {
            int j = 1;
            while (j <= 3)
            {
                System.out.print(j + " ");
                j++;
            }
            System.out.println();
            i++;
        }
    }
}

**Output:**

1 2 3  
1 2 3  
1 2 3  

---

**Important Points to Remember -**

• Nested loops increase the number of iterations  
• Inner loop executes fully for each outer loop iteration  
• Variable names should be chosen carefully  
• Used heavily in pattern and matrix problems  

---

**Summary:**

• Nested loops are loops inside loops  
• Used when repeated repetition is required  
• Commonly used for patterns and tables  
• Essential concept for DSA and problem solving
