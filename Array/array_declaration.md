
In Java, an array must be **declared** before it can be used and **initialized** before it can store values. Declaration
tells Java the type of data the array will store, while initialization allocates memory and assigns values to the array.

There are multiple ways to declare and initialize arrays in Java depending on the use case.

**1. Array Declaration -**

Array declaration specifies the **data type** of elements and the **array name**, but does not allocate memory.

Syntax:
dataType[] arrayName;

Example:

int[] numbers;
String[] names;

At this stage, the array is only declared and cannot store values until it is initialized.

---

**2. Array Initialization Using new Keyword -**

In this method, memory is allocated using the `new` keyword and the size of the array is specified.

Example:

class ArrayInitializationExample
{
    public static void main(String[] args)
    {
        int[] numbers = new int[5];

        numbers[0] = 10;
        numbers[1] = 20;
        numbers[2] = 30;
        numbers[3] = 40;
        numbers[4] = 50;

        System.out.println("Array elements:");
        for (int i = 0; i < numbers.length; i++)
        {
            System.out.println(numbers[i]);
        }
    }
}

**Output:**

Array elements:
10
20
30
40
50

Here, the array size is fixed at 5. Each element is assigned a value using its index.

---

**3. Array Initialization Using Literal Values -**

This is the most common and simplest way to initialize an array when values are already known.

Example:

class ArrayLiteralExample
{
    public static void main(String[] args)
    {
        int[] marks = {85, 90, 78, 92, 88};

        System.out.println("Marks array:");
        for (int i = 0; i < marks.length; i++)
        {
            System.out.println(marks[i]);
        }
    }
}

**Output:**

Marks array:
85
90
78
92
88

In this case, Java automatically determines the size of the array based on the number of values provided.

---

**4. Declaration and Initialization in Separate Steps -**

An array can also be declared first and initialized later.

Example:

class SeparateDeclarationExample
{
    public static void main(String[] args)
    {
        int[] values;
        values = new int[]{5, 10, 15, 20};

        System.out.println("Array values:");
        for (int i = 0; i < values.length; i++)
        {
            System.out.println(values[i]);
        }
    }
}

**Output:**

Array values:
5
10
15
20

This approach is useful when array values are decided at runtime.

---

**Important Points to Remember -**

• Array size is **fixed** once created.  
• Indexing starts from **0** and ends at `length - 1`.  
• Accessing an invalid index causes `ArrayIndexOutOfBoundsException`.  
• Default values:  
  • `0` for int  
  • `0.0` for double  
  • `false` for boolean  
  • `null` for objects  

---

**Summary:**

• Arrays must be **declared** before use.  
• Arrays must be **initialized** before storing values.  
• Initialization can be done using `new` or using literal values.  
• Array size cannot be changed after creation.  
