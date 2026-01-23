
**Definition:**

Command Line Arguments in Java are the values passed to a program at the time of execution. These values are received
by the `main` method through the `String[] args` parameter and allow the program to take input without using `Scanner`
or hardcoded values.

---

**Syntax of main Method with Command Line Arguments -**

public static void main(String[] args)

Here, `args` is an array of strings that stores the values passed from the command line.

---

**1. Simple Example of Command Line Arguments -**

Example:

class CommandLineExample
{
    public static void main(String[] args)
    {
        System.out.println("First argument: " + args[0]);
        System.out.println("Second argument: " + args[1]);
    }
}

**How to Run:**

java CommandLineExample Hello Java

**Output:**

First argument: Hello  
Second argument: Java  

Each word passed after the class name is treated as a separate argument.

---

**2. Accessing Multiple Command Line Arguments Using Loop -**

Command line arguments can be accessed using a loop since `args` is an array.

Example:

class CommandLineLoop
{
    public static void main(String[] args)
    {
        System.out.println("Command Line Arguments:");
        for (int i = 0; i < args.length; i++)
        {
            System.out.println(args[i]);
        }
    }
}

**How to Run:**

java CommandLineLoop One Two Three

**Output:**

Command Line Arguments:
One  
Two  
Three  

---

**3. Converting Command Line Arguments to Integer -**

Since command line arguments are strings, they must be converted to numeric types for calculations.

Example:

class CommandLineAddition
{
    public static void main(String[] args)
    {
        int a = Integer.parseInt(args[0]);
        int b = Integer.parseInt(args[1]);

        int sum = a + b;
        System.out.println("Sum = " + sum);
    }
}

**How to Run:**

java CommandLineAddition 10 20

**Output:**

Sum = 30  

---

**Important Points to Remember -**

• Command line arguments are always stored as strings  
• `args.length` gives the number of arguments  
• Indexing starts from `0`  
• Conversion is required for numeric operations  
• Accessing invalid index causes `ArrayIndexOutOfBoundsException`  

---

**Difference Between Scanner Input and Command Line Arguments -**

| Feature                  | Scanner Input           | Command Line Arguments |
|--------------------------|-------------------------|------------------------|
| Input time               | During program execution| At program start       |
| Input method             | Scanner                 | main method arguments  |
| Data type                | Any                     | String only            |
| User interaction         | Required                | Not required           |

---

**Summary:**

• Command line arguments allow input at execution time  
• They are accessed using `String[] args`  
• Useful for quick inputs and automation  
• Commonly used in testing and scripting
