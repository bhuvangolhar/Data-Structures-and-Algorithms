

 **Encapsulation in Java**

 **Definition**

* **Encapsulation** is the process of **binding data (variables)** and **methods (functions)** that operate on that data into a **single unit (class)**.
* It is often described as a **protective shield** that prevents direct access to the data and ensures controlled interaction.
* Encapsulation is achieved through:

  1. 
}
 

}

    public static void main(String[] args) {
        Student s1 = new Student();

      
        // Trying invalid value
        s1.setAge(-5);  // Will print validation message
    }
}


**Output:**


Name: Alice
Age: 20
Age must be positive!


 **Real-Life Analogy**

Think of **capsules in medicine**:

* The ingredients (data) are hidden inside the capsule.
* You only consume the capsule (methods) to interact with the medicine.
* You don’t get direct access to the raw ingredients.

Similarly, in Java:

* Data is hidden (`private fields`).
* Access i
* Extra boilerplate code (getters and setters).
* Overuse of getters/setters can reduce readability if not well-designed.


 **Example 2: Bank Account (Real-World Use Case)**

class BankAccount {
    private double balance;

    // Deposit money
    public void deposit(double amount) {
        if (amount > 0) {
            balance += amount;
            System.out.println("Deposited: " + amount);
        } else {
            System.out.println("Invalid deposit amount!");
        }
    }

    // Withdraw money
    public void withdraw(double amount) {
        if (amount > 0 && amount <= balance) {
            balance -= amount;
            System.out.println("Withdrew: " + amount);
        } else {
            System.out.println("Invalid or insufficient balance!");
        }
    }

    // Get balance
    public double getBalance() {
        return balance;
    }
}

public class BankDemo {
    public static void main(String[] args) {
        BankAccount acc = new BankAccount();

        acc.deposit(5000);
        acc.withdraw(2000);
        System.out.println("Current Balance: " + acc.getBalance());

        acc.withdraw(4000); // Invalid because balance < 4000
    }
}


**Output:**


Deposited: 5000.0
Withdrew: 2000.0
Current Balance: 3000.0
Invalid or insufficient balance!
 **When to Use Encapsulation**

* Whenever you need **controlled access** to class fields.
* When **sensitive data** should not be exposed directly (e.g., passwords, account balance).
* For **maintainability** – easier to refactor without breaking dependent code.


 **Conclusion**

* Encapsulation is about **binding data and methods** into a single unit (class).
* Achieved by **making fields private** and using **public getters/setters**.
* It provides **security, flexibility, and maintainability**.
* Along with **inheritance and polymorphism**, encapsulation makes Java OOP **robust and reliable**.

