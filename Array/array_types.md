
 Array Types in Java

Arrays in Java are used toy (1D Array)

    
}
cial type of 2D array where each row can have a different number of columns.
This makes it **non-rectangular**.

 Example:

public class JaggedArray {
    public static void main(String[] args) {
        // Declaration
        int[][] jagged = new int[3][];

    

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
| Performance |
Arrays are **faster and memory-efficient**, but **Collections** (like `ArrayList`) provide **more flexibility**.

