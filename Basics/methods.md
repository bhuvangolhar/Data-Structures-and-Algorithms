
**Definition :**

A method in Java is a block of code that performs a specific task.
It is used to group statements together, so they can be executed
whenever the method is called. Methods improve reusability, readability,
and modularity in a program.

**Syntax :**

returnType methodName(parameters)
{
*// method body*
*// statements*
return value; *// if returnType is not void*
}

**Examples :**

int add(int a, int b)
{
return a + b;
}

void greet()
{
System.out.println("Hello, Java!");
}

**Rules :**

→ Must be declared inside a class.
→ Method name should follow Java naming rules (start with lowercase, meaningful name).
→ If the method returns a value, returnType must not be void.
→ Parameters are optional; methods can have zero or many parameters.
→ main() is the entry point method of every Java program.

**Types :**

▪ Predefined Methods – Already defined in Java libraries (e.g., Math.max(), System.out.println()).
▪ User-defined Methods – Created by the programmer to perform specific tasks.
▪ Static Methods – Declared with static, can be called without creating an object.
▪ Instance Methods – Belong to an object, need an object to call.

**Program :**

class MethodsDemo
{
*// user-defined method*
int multiply(int x, int y)
{
return x \* y;
}
*// static method*
sobj.multiply(5, 4);
System.out.println("Multiplication: " + result);
*// calling static method*
displayMessage();
}
}

**Output :**

Multiplication: 20
