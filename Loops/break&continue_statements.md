
**Definition:**

The **`break`** and **`continue`** are **loop control statements** used to change the normal flow of loops. They help control when a
loop should stop or skip certain iterations.

---

**1. break Statement -**

The `break` statement is used to terminate the loop immediately when a specific condition is met.

Example:

class BreakExample
{
    public static void main(String[] args)
    {
        for (int i = 1; i <= 5; i++)
        {
            if (i == 3)
            {
                break;
            }
            System.out.println(i);
        }
    }
}

**Output:**

1  
2  

When `i` becomes 3, the loop stops completely.

---

**2. continue Statement -**

The `continue` statement is used to skip the current iteration and continue with the next iteration of the loop.

Example:

class ContinueExample
{
    public static void main(String[] args)
    {
        for (int i = 1; i <= 5; i++)
        {
            if (i == 3)
            {
                continue;
            }
            System.out.println(i);
        }
    }
}

**Output:**

1  
2  
4  
5  

When `i` is 3, that iteration is skipped.

---

**3. break in while Loop -**

Example:

class BreakWhileExample
{
    public static void main(String[] args)
    {
        int i = 1;
        while (i <= 5)
        {
            if (i == 4)
            {
                break;
            }
            System.out.println(i);
            i++;
        }
    }
}

**Output:**

1  
2  
3  

---

**4. continue in while Loop -**

Example:

class ContinueWhileExample
{
    public static void main(String[] args)
    {
        int i = 0;
        while (i < 5)
        {
            i++;
            if (i == 3)
            {
                continue;
            }
            System.out.println(i);
        }
    }
}

**Output:**

1  
2  
4  
5  

---

**Important Points to Remember -**

• `break` exits the loop completely  
• `continue` skips only the current iteration  
• Both are commonly used with conditions  
• They improve control over loop execution  
• Overuse can reduce readability  

---

**Summary:**

• Loop control statements manage loop execution  
• `break` stops the loop  
• `continue` skips an iteration  
• Used with all loop types in Java
