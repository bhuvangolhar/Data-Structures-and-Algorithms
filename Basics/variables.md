
**Definiton:**

A variable is like a container in memory that stores data.
Every variable has :
- a name (identifier)
- a type (what kind of data it can store)
- a value (the actual data stored)

**Syntax:**

dataType variableName = value;

**Examples:**

int age = 22;                     // *integer value*
double pi = 3.14;                // *decimal value*
char grade = 'A';               // *single character*
String name = "Bhuvan";        // *text (sequence of characters)*
boolean isStudent = true;     // *true or false value*

**Rules:**

- Must begin with a letter, underscore(_), or $.
- Cannot start with a digit.
- Case sensitive (Age and age are different).
- Should be meaningful (use marks instead of m).
- Cannot use Java keywords (int, class, for etc.).

**Types:**

1) Local Variable – declared inside a method, accessible only there.
2) Instance Variable – declared inside a class but outside methods (belongs to an object).
3) Static Variable – declared with static, belongs to the class (common for all objects).

**Program:**

class VariablesDemo
{
    int instanceVar = 100;          // *instance variable*
    static int staticVar = 200;    // *static variable*
    void display() 
    {
        int localVar = 50;      // *local variable*
        System.out.println("Local Variable: " + localVar);
        System.out.println("Instance Variable: " + instanceVar);
        System.out.println("Static Variable: " + staticVar);
    }
    public static void main(String[] args)
    {
        VariablesDemo obj = new VariablesDemo();
        obj.display();
    }
}

**Output:**

Local Variable: 50
Instance Variable: 100
Static Variable: 200

