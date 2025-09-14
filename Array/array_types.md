
 Array Types in Java

Arrays in Java are used to store **multiple elements of the same type** in a single variable. Based on structure and usage, arrays in Java can be broadly classified into three categories:

 1. Single-Dimensional Array (1D Array)

A **1D array** is the simplest type of array.
It stores data in a **linear form** (one row, multiple columns).

Example:


public class Singln
        int[] arr = {10, 20, 30, 40, 50};

        // Traversal
        for (int i = 0; i < arr.length; i++) {
            System.out.println("Element at index " + i + ": " + arr[i]);
        }
    }
}

 Key Points:

* Index starts at `0` and goes till `n-1`.
* Access is **O(1)** using `arr[index]`.
* Used for storing simple lists (marks, prices, scores, etc.).

 2. Multi-Dimensional Array (2D Array and more)

A **multi-dimensional array** is an array of arrays.
The most common form is the **2D array** (like a matrix or table).

 Example (2D Array):

public class TwoDArray {
    public static void main(String[] args) {
        // Declaration and initialization
        int[][] matrix = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };

        // Traversal
        for (int i = 0; i < matrix.length; i++) {
            for (int j = 0; j < matrix[i].length; j++) {
                System.out.print(matrix[i][j] + " ");
         
}

 Key Points:

* `matrix[i][j]` → element at row `i` and column `j`.
* Commonly used in:

  * **Matrix problems**
  * **Grids in games**
  * **Dynamic Programming (DP) tables**

 3. Jagged Array (Array of Arrays)

A **jagged array** is a special type of 2D array where each row can have a different number of columns.
This makes it **non-rectangular**.

 Example:

public class JaggedArray {
    public static void main(String[] args) {
        // Declaration
        int[][] jagged = new int[3][];

    

        // Traversal
        for (int i = 0; i < jagged.length; i++) {
            for (int j = 0; j < jagged[i].length; j++) {
                System.out.print(jagged[i][j] + " ");
            }
            System.out.println();
        }
    }
}

 Key Points:

* Each row has a different length.
* Useful when data is naturally irregular (like storing marks of students where each student appeared for different number of subjects).

 Arrays vs Collections

| Feature     | Arrays                    | Collections (ArrayList, etc.)            |
| ----------- | ------------------------- | ---------------------------------------- |
| Size        | Fixed                     | Dynamic                                  |
| Data type   | Same                      | Can use Generics (Object types)          |
| Performance | Faster for primitive data | Slower (boxing/unboxing overhead)        |
| Flexibility | Rigid                     | More flexible (resize, built-in methods) |



 Summary

* **Single-Dimensional Array** → Linear, simple list.
* **Multi-Dimensional Array** → Grids, matrices, DP problems.
* **Jagged Array** → Non-rectangular, irregular data.

Arrays are **faster and memory-efficient**, but **Collections** (like `ArrayList`) provide **more flexibility**.

