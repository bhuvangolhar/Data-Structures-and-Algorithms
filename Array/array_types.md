jjjaj
In Java, arrays are mainly of three types — **one-dimensional**, **two-dimensional**, and **jagged arrays**. A one-
dimensional array stores data in a single row, a two-dimensional array stores data in rows and columns like a table,
and a jagged array is a special type of 2D array where each row can have a different number of elements.

**1. One-Dimensional Array (1D Array) -**

A **one-dimensional array** is the simplest type of array in Java. It stores data in a single row or a single line, where 
each element can be accessed by one index. You can think of it like a list of values placed side by side.

class OneDArrayExample 
{
    public static void main(String[] args) 
    {
        int[] marks = {85, 90, 78, 92, 88};
        System.out.println("1D Array elements:");
        for (int i = 0; i < marks.length; i++) 
        {
            System.out.println("Element at index " + i + " = " + marks[i]);
        }
    }
}

**Output:**

1D Array elements:
Element at index 0 = 85
Element at index 1 = 90
Element at index 2 = 78
Element at index 3 = 92
Element at index 4 = 88

In this example, `marks` is a one-dimensional array that stores five integer values.

**2. Two-Dimensional Array (2D Array) -**

A **two-dimensional array** stores data in the form of rows and columns, similar to a table or a matrix. You can think of it 
as an array of arrays — each element of the main array is itself another array.

class TwoDArrayExample 
{
    public static void main(String[] args) 
    {
        int[][] matrix = 
        {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };
        System.out.println("2D Array elements:");
        for (int i = 0; i < matrix.length; i++) 
        {
            for (int j = 0; j < matrix[i].length; j++) 
            {
                System.out.print(matrix[i][j] + " ");
            }
            System.out.println(); // move to next line after each row
        }
    }
}

**Output:**

2D Array elements:
1 2 3 
4 5 6 
7 8 9 

Here, `matrix` is a two-dimensional array with 3 rows and 3 columns. You access elements using two indices — one for the row
and one for the column (for example, `matrix[1][2]` gives `6`).

**3. Jagged Array (Array of Arrays) -**

A **jagged array** (also called a **ragged array**) is a special type of two-dimensional array where each row can have a 
*different number of columns*. Unlike a regular 2D array, the rows in a jagged array are not required to be of equal 
length.

class JaggedArrayExample 
{
    public static void main(String[] args) 
    {
        int[][] jagged = new int[3][];  // 3 rows, but columns not fixed
        jagged[0] = new int[]{1, 2, 3};
        jagged[1] = new int[]{4, 5};
        jagged[2] = new int[]{6, 7, 8, 9};
        System.out.println("Jagged Array elements:");
        for (int i = 0; i < jagged.length; i++) 
        {
            for (int j = 0; j < jagged[i].length; j++) 
            {
                System.out.print(jagged[i][j] + " ");
            }
            System.out.println();
        }
    }
}

**Output:**

Jagged Array elements:
1 2 3 
4 5 
6 7 8 9 

In this example, the first row has 3 elements, the second has 2, and the third has 4. This shows how jagged arrays allow 
flexible row sizes, unlike regular 2D arrays.

**Summary:**

* A **1D array** stores data in a single row (like a simple list).
* A **2D array** stores data in rows and columns (like a table).
* A **jagged array** stores data in multiple rows where each row can have a different number of columns (like uneven rows of
*  data).
