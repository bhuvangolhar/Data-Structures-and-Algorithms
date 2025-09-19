
Do-While Loop

Definition :

A do-while loop in Java executes a block of code at least once, and then keeps repeating it as long as the given condition is true.

It is an exit-controlled loop, because the condition is checked after executing the loop body.

This makes it different from the while loop, which checks the condition first.

Need :

Used when you want the code to run at least once, even if the condition is false.
ute
} 
while (condition);


Example :

class DoWhileLoopDemo 
{
    public static void main(String[] args) 
    {
        int num = 1;
        do 
        {
     
        } 
    
}


Output :

Number: 1
Number: 2
Number: 3


The loop body runs once before the condition is checked.

If the condition is false on the first check, the loop still executes one time.

