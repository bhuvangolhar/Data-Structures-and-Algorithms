
**Definition:**

**Type casting** in Java means converting one data type into another. It allows you to assign a value of one type to a
variable of another type. Since Java is a strongly typed language, it does not automatically allow incompatible data
types to mix, but type casting gives you a controlled way to perform such conversions. It is commonly used when performing
calculations between different numeric types or when working with objects in inheritance hierarchies.

Type casting ensures that the program can handle different types of data efficiently without losing control over how data is
stored or interpreted. It is mainly divided into two categories — *Primitive Type Casting* and *Reference Type Casting*.

**1. Primitive Type Casting -**

Primitive type casting deals with converting one primitive data type into another (like `int`, `float`, `double`, `byte`, etc.).
There are two main kinds of primitive type casting — Widening (Implicit) and Narrowing (Explicit).

a) **Widening Type Casting (Implicit Casting) -**

Widening happens automatically when a smaller data type is converted into a larger data type. It is also called *upcasting*
because data moves from a lower range to a higher range without data loss.

The compiler performs this conversion automatically since there is no risk of losing information.

**Example:**

▪ int num = 10;
▪ double d = num;          // int is converted to double automatically
▪ System.out.println(d);  // Output: 10.0

Here, `int` is automatically converted to `double` because `double` can hold larger values and more precision.

**Conversion Order (Small → Big):**

`byte → short → int → long → float → double`

b) **Narrowing Type Casting (Explicit Casting) -**

Narrowing happens manually when a larger data type is converted into a smaller data type. It is also called *downcasting*
because data moves from a higher range to a lower range, and there might be loss of data or precision.

You must explicitly write the target type in parentheses to tell the compiler you are aware of the conversion.

**Example:**

▪ double d = 9.78;
▪ int num = (int) d;         // Explicitly converting double to int
▪ System.out.println(num);  // Output: 9

Here, the decimal part (`.78`) is lost because `int` cannot hold fractional values.

**Conversion Order (Big → Small):**

`double → float → long → int → short → byte`

**2. Reference Type Casting -**

Reference type casting applies to *objects* and deals with *inheritance*. It allows an object of one class type to be treated
as another type within the same inheritance hierarchy.

There are two kinds of reference casting — Upcasting & Downcasting.

a) **Upcasting -**

Upcasting means converting a subclass object into a superclass reference. It is done automatically by Java because every
subclass object “is a kind of” its superclass. Upcasting is used when you want to generalize code or call overridden methods.

**Example:**

class Animal
{
    void sound()
    {
        System.out.println("Animal makes a sound");
    }
}
class Dog extends Animal
{
    void sound()
    {
        System.out.println("Dog barks");
    }
}
public class Test
{
    public static void main(String[] args)
    {
        Animal a = new Dog();  // Upcasting
        a.sound();            // Output: Dog barks
    }
}

Here, 'Dog' is upcast to "Animal". Even though the reference is of type "Animal", the actual method of 'Dog' is executed
because of runtime polymorphism.

b) **Downcasting -**

Downcasting is the reverse of upcasting — it means converting a superclass reference back into a subclass type.
It must be done manually using explicit casting, and it should be done carefully because if the object is not truly
of the subclass type, it can cause a runtime error (`ClassCastException`).

**Example:**

▪ Animal a = new Dog();  // Upcasting
▪ Dog d = (Dog) a;      // Downcasting
▪ d.sound();           // Output: Dog barks

Here, downcasting allows access to subclass-specific features or methods that are not available in the superclass.

**Why Type Casting is Important?**

→ Type casting allows flexibility while maintaining Java’s strict type safety. It helps when:

▪ Performing mixed-type calculations (like `int` + `double`)
▪ Storing or retrieving objects in inheritance-based code
▪ Working with APIs that return general object types (`Object` class)
▪ Avoiding redundant code by treating different data types uniformly

**In Short:**

| Type                     | Direction             | Automatic / Manual | Data Loss      | Example                           |
| ------------------------ | --------------------- | ------------------ | -------------- | --------------------------------- |
| **Widening (Implicit)**  | Small → Big           | Automatic          | No             | `int a = 10; double b = a;`       |
| **Narrowing (Explicit)** | Big → Small           | Manual             | Yes (possible) | `double d = 9.7; int i = (int)d;` |
| **Upcasting**            | Subclass → Superclass | Automatic          | No             | `Animal a = new Dog();`           |
| **Downcasting**          | Superclass → Subclass | Manual             | Possible error | `Dog d = (Dog)a;`                 |
