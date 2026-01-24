
**Definition:**

**Pattern programs** are programs that use *loops (mostly nested loops)* to print shapes using characters, numbers or
symbols. They help improve logical thinking, loop control and problem-solving skills.

Pattern programs are very important for interviews and competitive programming.

---

**1. Star Pattern (Square Pattern) -**

Example:

class SquareStarPattern
{
    public static void main(String[] args)
    {
        for (int i = 1; i <= 4; i++)
        {
            for (int j = 1; j <= 4; j++)
            {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}

**Output:**

* * * *  
* * * *  
* * * *  
* * * *  

---

**2. Right-Angled Triangle Pattern -**

Example:

class RightTrianglePattern
{
    public static void main(String[] args)
    {
        for (int i = 1; i <= 4; i++)
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
* * * *  

---

**3. Inverted Triangle Pattern -**

Example:

class InvertedTrianglePattern
{
    public static void main(String[] args)
    {
        for (int i = 4; i >= 1; i--)
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

* * * *  
* * *  
* *  
*  

---

**4. Number Pattern -**

Example:

class NumberPattern
{
    public static void main(String[] args)
    {
        for (int i = 1; i <= 4; i++)
        {
            for (int j = 1; j <= i; j++)
            {
                System.out.print(j + " ");
            }
            System.out.println();
        }
    }
}

**Output:**

1  
1 2  
1 2 3  
1 2 3 4  

---

**5. Pyramid Pattern -**

Example:

class PyramidPattern
{
    public static void main(String[] args)
    {
        for (int i = 1; i <= 4; i++)
        {
            for (int j = 4; j > i; j--)
            {
                System.out.print(" ");
            }
            for (int k = 1; k <= i; k++)
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
* * * *  

---

**Important Points to Remember -**

• Pattern programs mainly use nested loops  
• Outer loop controls rows  
• Inner loop controls columns  
• Spacing is important for alignment  
• Helps build strong loop logic  

---

**Summary:**

• Pattern programs improve logical thinking  
• They rely on nested loops  
• Widely asked in interviews  
• Form the base for complex DSA problems
