
**Definiton :**

A variable is like a container in memory that stores data.
Every variable has like,
- a name (identifier)
- a type (what kind of data it can store)
- a value (the actual data stored)

**Syntax :**

dataType variableName = value;

**Examples :**

int age = 22;                     // *integer value*
double pi = 3.14;                // *decimal value*

- Should be meaningful (use marks instead of m).
- Cannot use Java keywords (int, class, for etc.).

**Types :**

1) Local Variable – declared inside a method, accessible only there.
2) Instance Variable – declared inside a class but outside methods (belongs to an object).
3) Static Variable – declared with static, belongs to the class (common for all objects).

**Program :**

class VariablesDemo
{
    int instanceVar = 100;          // *instance variable*
    static int staticVar = 200;    // *static variable*
    void display() 
    {
        
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

**Output :**

Local Variable : 50
Instance Variable : 100
Static Variable : 200
