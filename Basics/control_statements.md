
**Definition:**

Control statements in Java are used to **control the flow of execution** of a program. They decide which statements
should be executed and how many times they should be executed based on conditions. Control statements make programs
logical, dynamic, and decision-based instead of running line by line without choice.

Java provides different types of control statements to handle decision making, looping, and branching.

---

**Types of Control Statements:**

Java control statements are mainly divided into three categories:

1. Decision-Making Statements  
2. Looping Statements  
3. Branching Statements  

---

**1. Decision-Making Statements -**

Decision-making statements allow the program to choose different paths based on conditions.

**a) if Statement -**

The `if` statement executes a block of code only when a given condition is true.

Example:

• int age = 18;  
• if (age >= 18)  
• {  
•     System.out.println("Eligible to vote");  
• }  

**Explanation:**

If the condition inside `if` is true, the code block executes; otherwise, it is skipped.

---

**b) if-else Statement -**

The `if-else` statement provides an alternative block of code when the condition is false.

Example:

• int number = 5;  
• if (number % 2 == 0)  
• {  
•     System.out.println("Even number");  
• }  
• else  
• {  
•     System.out.println("Odd number");  
• }  

---

**c) if-else-if Ladder -**

This is used when multiple conditions need to be checked.

Example:

• int marks = 72;  
• if (marks >= 90)  
•     System.out.println("Grade A");  
• else if (marks >= 75)  
•     System.out.println("Grade B");  
• else if (marks >= 60)  
•     System.out.println("Grade C");  
• else  
•     System.out.println("Fail");  

---

**d) switch Statement -**

The `switch` statement is used when there are multiple fixed choices.

Example:

• int day = 3;  
• switch (day)  
• {  
•     case 1: System.out.println("Monday"); break;  
•     case 2: System.out.println("Tuesday"); break;  
•     case 3: System.out.println("Wednesday"); break;  
•     default: System.out.println("Invalid day");  
• }  

---

**2. Looping Statements -**

Looping statements are used to execute a block of code repeatedly.

**a) for Loop -**

Used when the number of iterations is known.

Example:

• for (int i = 1; i <= 5; i++)  
• {  
•     System.out.println(i);  
• }  

---

**b) while Loop -**

Used when the condition is checked before execution.

Example:

• int i = 1;  
• while (i <= 5)  
• {  
•     System.out.println(i);  
•     i++;  
• }  

---

**c) do-while Loop -**

Ensures that the loop executes at least once.

Example:

• int i = 1;  
• do  
• {  
•     System.out.println(i);  
•     i++;  
• }  
• while (i <= 5);  

---

**3. Branching Statements -**

Branching statements are used to transfer control from one part of the program to another.

**a) break Statement -**

Used to exit a loop or switch statement immediately.

Example:

• for (int i = 1; i <= 5; i++)  
• {  
•     if (i == 3)  
•         break;  
•     System.out.println(i);  
• }  

---

**b) continue Statement -**

Used to skip the current iteration and continue with the next one.

Example:

• for (int i = 1; i <= 5; i++)  
• {  
•     if (i == 3)  
•         continue;  
•     System.out.println(i);  
• }  

---

**Summary:**

• Control statements decide the execution flow of a program.  
• Decision-making statements handle conditions.  
• Looping statements repeat execution.  
• Branching statements alter normal flow.  
• Control statements are essential for writing logical and real-world Java programs.

---

**Importance of Control Statements:**

Without control statements, Java programs would execute linearly without logic or decisions. Control statements enable
Java programs to behave intelligently by responding to different inputs and conditions.
