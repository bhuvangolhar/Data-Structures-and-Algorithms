
**Array traversal** means accessing and processing each element of an array one by one. Traversal is a fundamental
operation because almost all array problems involve visiting elements to read, modify or display them.

In Java, arrays can be traversed using different looping techniques.

---

**1. Traversal Using for Loop -**

The `for` loop is the most commonly used method to traverse an array when the index is required.

Example:

class ArrayTraversalForLoop
{
    public static void main(String[] args)
    {
        int[] numbers = {10, 20, 30, 40, 50};

        System.out.println("Array elements using for loop:");
        for (int i = 0; i < numbers.length; i++)
        {
            System.out.println(numbers[i]);
        }
    }
}

**Output:**

Array elements using for loop:
10
20
30
40
50

Here, the loop starts from index `0` and runs until `length - 1`.

---

**2. Traversal Using for-each Loop -**

The **for-each loop** (also called enhanced for loop) is simpler and is used when the index is not required.

Example:

class ArrayTraversalForEach
{
    public static void main(String[] args)
    {
        int[] numbers = {5, 15, 25, 35};

        System.out.println("Array elements using for-each loop:");
        for (int num : numbers)
        {
            System.out.println(num);
        }
    }
}

**Output:**

Array elements using for-each loop:
5
15
25
35

In this loop, `num` directly stores the value of each array element.

---

**3. Traversal Using while Loop -**

A `while` loop can also be used to traverse an array when the condition needs to be checked explicitly.

Example:

class ArrayTraversalWhileLoop
{
    public static void main(String[] args)
    {
        int[] values = {2, 4, 6, 8};

        int i = 0;
        System.out.println("Array elements using while loop:");
        while (i < values.length)
        {
            System.out.println(values[i]);
            i++;
        }
    }
}

**Output:**

Array elements using while loop:
2
4
6
8

---

**Important Points to Remember -**

• Array traversal always starts from index **0**.  
• The last valid index is `array.length - 1`.  
• Using an invalid index causes `ArrayIndexOutOfBoundsException`.  
• `for-each` loop is read-only and cannot modify array indices.  
• Use `for` loop when index-based access is required.

---

**Summary:**

• Array traversal means visiting each element of an array.  
• Java provides multiple ways to traverse arrays.  
• `for` loop is best when index is needed.  
• `for-each` loop is simpler for reading values.  
• Traversal is the foundation of searching and sorting algorithms.
