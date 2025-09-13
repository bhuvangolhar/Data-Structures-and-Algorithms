
Enhanced For Loop (For-Each Loop)

Definition :

The enhanced for loop (also called the for-each loop) in Java is a simplified version of the for loop.

It is mainly used to iterate through arrays or collections without using an index.

It makes code cleaner, shorter, and easier to read compared to a traditional for loop.

Need :

When you want to access every element of an array or collection sequentially.

Reduces chances of errors since you don’t need to manage loop counters or conditions.

Best choice for read-only access of elements.

Syntax :

for (dataType variable : arrayOrCollection) 
{
    // code block using variable
}


Example with Array :

class ForEachLoopDemo 
{
    public static void main(String[] args) 
    {
        int numbers[] = {10, 20, 30, 40, 50};
        for (int num : numbers) 
        {
            System.out.println("Number: " + num);
        }
   


Example with String Array :

class ForEachStringDemo 
{
    public static void main(String[] args) 
    {
        String names[] = {"Alice", "Bob", "Charlie"};
        for (String name : names) 
        {
            System.out.println("Hello, " + name);
        }
    }
}


Output :

Hello, Alice
Hello, Bob
Hello, Charlie


Key Notes :

Works with arrays and collections (like ArrayList, HashSet).

Cannot directly modify elements of an array/collection (read-only).

Useful for simple iteration, not when index manipulation is required.
