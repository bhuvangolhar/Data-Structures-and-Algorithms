
In real-world programs and competitive programming, array values are often taken *from the user at runtime* instead of
being hardcoded. Java provides the `Scanner` class to take input from the user.

---

**1. Taking Array Input Using Scanner -**

In this method, the user first enters the size of the array, followed by the elements.

Example:

import java.util.Scanner;

class ArrayInputExample
{
    public static void main(String[] args)
    {
        Scanner scan = new Scanner(System.in);

        System.out.print("Enter the size of the array: ");
        int size = scan.nextInt();

        int[] numbers = new int[size];

        System.out.println("Enter array elements:");
        for (int i = 0; i < size; i++)
        {
            numbers[i] = scan.nextInt();
        }

        System.out.println("Array elements are:");
        for (int i = 0; i < numbers.length; i++)
        {
            System.out.println(numbers[i]);
        }
    }
}

**Output:**

Enter the size of the array: 4  
Enter array elements:  
10  
20  
30  
40  

Array elements are:
10  
20  
30  
40  

---

**2. Array Input Using for-each Loop (Display Only) -**

The `for-each` loop is commonly used to **display array values**, not for taking input.

Example:

class ArrayForEachDisplay
{
    public static void main(String[] args)
    {
        int[] values = {3, 6, 9, 12};

        System.out.println("Array elements:");
        for (int num : values)
        {
            System.out.println(num);
        }
    }
}

**Output:**

Array elements:
3  
6  
9  
12  

---

**Important Points to Remember -**

• Array size must be known before taking input.  
• Array elements are stored using index positions.  
• Input is usually taken using a `for` loop.  
• `for-each` loop cannot be used to insert values.  
• User input makes programs dynamic and flexible.

---

**Summary:**

• Arrays can take input from the user using `Scanner`.  
• The size of the array is entered first.  
• A loop is used to store elements in the array.  
• Input-based arrays are widely used in DSA problems.
