
Definition :

A while loop in Java is used to repeatedly execute a block of code as long as a given condition is true.

It checks the condition before executing the loop body, making it an entry-controlled loop.

This loop is useful when the number of iterations is not known in advance and depends on some condition during runtime.

Need :

Used when you want to keep running a task until a condition changes.

Helps avoid repetition of code.

Useful in scenarios like reading input until "exit" is entered, waiting for a condition to become false, etc.

Syntax :

while (condition) 
{
    // code block
    // statements to execute
}


Example :

class WhileLoopDemo 
{
    public static void main(String[] args) 
    {
        int count = 1;
        while (count <= 5) 
        {
            System.out.println("Count: " + count);
            count++;
        }
    }
}


Output :

Count: 1
Count: 2
Count: 3
Count: 4
Count: 5


Key Notes :

Condition is checked before entering the loop body.

If the condition is false initially, the loop body may not execute even once.

Make sure the loop has a way to terminate, otherwise it can run infinitely.
