
**Definition:**

**Wrapper classes** in Java are used to convert primitive data types into objects. Each primitive data type has a
corresponding wrapper class that allows it to be treated as an object.

Wrapper classes are part of the `java.lang` package.

---

**Why Wrapper Classes Are Needed?**

- To use primitive values as objects  
- To work with Java collections (which store objects only)  
- To perform object-based operations  
- To convert strings into numeric values  

---

**Primitive Types and Their Wrapper Classes -**

| Primitive Data Type | Wrapper Class |
|---------------------|---------------|
| int                 | Integer       |
| double              | Double        |
| char                | Character     |
| boolean             | Boolean       |
| byte                | Byte          |
| short               | Short         |
| long                | Long          |
| float               | Float         |

---

**1. Converting Primitive to Wrapper Object (Boxing) -**

Boxing is the process of converting a primitive data type into its corresponding wrapper object.

Example:

class BoxingExample
{
    public static void main(String[] args)
    {
        int num = 10;
        Integer obj = Integer.valueOf(num);

        System.out.println(obj);
    }
}

**Output:**

10

---

**2. Converting Wrapper Object to Primitive (Unboxing) -**

Unboxing is the process of converting a wrapper object back into a primitive data type.

Example:

class UnboxingExample
{
    public static void main(String[] args)
    {
        Integer obj = 20;
        int num = obj.intValue();

        System.out.println(num);
    }
}

**Output:**

20

---

**3. Autoboxing and Auto-unboxing -**

Java automatically converts primitives to wrapper objects and vice versa. This feature is called autoboxing and
auto-unboxing.

Example:

class AutoBoxingExample
{
    public static void main(String[] args)
    {
        Integer a = 15;   // autoboxing
        int b = a;       // auto-unboxing

        System.out.println(a);
        System.out.println(b);
    }
}

**Output:**

15  
15  

---

**4. Wrapper Classes and String Conversion -**

Wrapper classes provide methods to convert strings into primitive values.

Example:

class StringConversionExample
{
    public static void main(String[] args)
    {
        int a = Integer.parseInt("10");
        double b = Double.parseDouble("5.5");

        System.out.println(a + b);
    }
}

**Output:**

15.5  

---

**Important Points to Remember -**

- Wrapper classes store primitive values as objects  
- They are immutable (cannot be changed once created)  
- Autoboxing simplifies conversion automatically  
- Parsing methods help convert strings to numbers  
- Wrapper classes are widely used in real Java programs  

---

**Summary:**

- Wrapper classes bridge primitive types and objects  
- Each primitive type has a corresponding wrapper class  
- Boxing and unboxing convert between primitives and objects  
- Wrapper classes enable advanced Java features
