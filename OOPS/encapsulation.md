/.\

**Definition:**

**Encapsulation** is one of the fundamental principles of Object-Oriented Programming System (OOPs) in Java. It refers to
the *wrapping (or binding) of data and methods* that operate on that data into a single unit, typically a class.
In simpler terms, encapsulation is like putting data (variables) and code (methods) that work on that data inside a capsule 
(the class) — protecting it from direct access and misuse. It ensures that an object’s internal state is hidden from the 
outside world, and can only be accessed through *controlled interfaces* (i.e. getters and setters). Encapsulation is 
the process of hiding the internal details of an object from the outside and only allowing access to it through public 
methods. This is also known as data hiding.

**Key Ideas:**

‣ The data (variables) of a class are kept private so that they cannot be accessed directly from outside the class.
‣ To read or modify these variables, public methods (getters and setters) are provided.

**Syntax Example:**

class ClassName 
{
    private dataType variableName;
    // private data
    // Public setter method - to set value
    public void setVariableName(dataType value) 
    {
        variableName = value;
    }
    // Public getter method - to get value
    public dataType getVariableName() 
    {
        return variableName;
    }
}

**Example:**

class Student 
{
    // Private data members - hidden from outside access
    private String name;
    private int age;
    // Setter method for name
    public void setName(String n) 
    {
        name = n;
    }
    // Getter method for name
    public String getName() 
    {
        return name;
    }
    // Setter method for age
    public void setAge(int a) 
    {
        // validation
        if (a > 0) 
        {        
            age = a;
        }
    }
    // Getter method for age
    public int getAge() 
    {
        return age;
    }
}
class Example 
{
    public static void main(String[] args) 
    {
        Student s = new Student();
        s.setName("John");
        // setting value using setter
        s.setAge(20);
        System.out.println("Name: " + s.getName());
        System.out.println("Age: " + s.getAge());
    }
}

**Output:**

Name: John
Age: 20

**Explanation:**

‣ The **variables** `name` and `age` are declared `private`, so they cannot be accessed directl from outside the
  `Student` class.
‣ Instead, the program uses public setter methods (`setName()`, `setAge()`) to assign values and getter methods
  (`getName()`, `getAge()`) to retrieve them.
‣ This ensures that only **valid data** enters the object, and the internal details remain secure & controlled.

**Advantages:**

1. **Data Hiding -** Prevents direct access to data and protects it from unintended modification.
2. **Improved Security -** Internal implementation details are hidden from the user.
3. **Control Over Data -** Through getters and setters, you can validate and control how data is accessed or changed.
4. **Code Flexibility and Maintenance -** You can modify internal implementation without affecting external code that
     uses the class.
5. **Better Organization -** Combines data and methods logically within a single class.

**Real-Life Analogy:**

Think of a **capsule** or **ATM machine** -

‣ You cannot directly access the money inside (private data).
‣ You can only interact with it using buttons (public methods) that perform controlled operations like withdrawing 
  or depositing.

**Key Points:**

‣ Achieved mainly using private variables and public methods.
‣ Provides the foundation for data security and modularity in Java programs.
‣ A well-encapsulated class hides unnecessary details and exposes only what is needed.

In summary, **Encapsulation** in Java ensures that the data of an object is safe, secure, and accessed in a controlled 
manner, making programs more robust, maintainable, and less error-prone.
