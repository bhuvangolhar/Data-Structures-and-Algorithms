
**Definition:**

The **for-each loop**, also known as the **enhanced for loop**, is a simplified version of the traditional `for` loop 
introduced in `Java 5 (JDK 1.5)`. It is mainly used for iterating through arrays or collections (like ArrayList, HashSet 
etc.) without the need for an explicit counter or index variable. The for-each loop makes code *cleaner, safer & more 
readable*, especially when you just want to access each element in a collection rather than modify its structure.

**Syntax:**

for (dataType variable : collectionOrArray) 
{
    // Code to be executed
}

**Explanation of Components:**

a) **dataType** – The type of elements stored in the array or collection (e.g., `int`, `String`, `double`).

b) **variable** – A temporary variable that holds each element during iteration.

c) **collectionOrArray** – The array or collection whose elements are to be accessed one by one.

**Flow of Execution:**

1] The loop starts by picking the *first element* from the array or collection and assigning it to the loop variable.

2] The body of the loop executes using that element.

3] Then it moves to the *next element*, repeating the process until all elements have been processed.

4] The loop automatically stops after reaching the *last element* — no need for a condition or counter.

**Example with Array:**

class Example 
{
    public static void main(String[] args) 
    {
        int numbers[] = {10, 20, 30, 40, 50};
        for (int num : numbers) 
        {
            System.out.println("Number: " + num);
        }
    }
}

**Output:**

Number: 10

Number: 20

Number: 30

Number: 40

Number: 50

**Example with Collection (ArrayList):**

import java.util.*;

class Example 
{
    public static void main(String[] args) 
    {
        ArrayList<String> names = new ArrayList<>();
        names.add("Alice");
        names.add("Bob");
        names.add("Charlie");
        for (String name : names) 
        {
            System.out.println("Name: " + name);
        }
    }
}

**Output:**

Name: Alice

Name: Bob

Name: Charlie

**Key Points:**

– The for-each loop is ideal for *read-only access* to elements of arrays or collections.

– It *cannot modify* the underlying structure of a collection (e.g., cannot remove elements during iteration).

– It *does not use an index*, so you cannot directly access the position of an element.

– It helps prevent *off-by-one errors* common in traditional for loops.

– Internally, the loop uses the *Iterator* interface for collections and *index-based iteration* for arrays.
