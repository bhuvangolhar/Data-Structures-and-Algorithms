

 **Encapsulation in Java**

 **Definition**

* **Encapsulation** is the process of **binding data (variables)** and **methods (functions)** that operate on that data into a **single unit (class)**.
* It is often described as a **protective shield** that prevents direct access to the data and ensures controlled interaction.
* Encapsulation is achieved through:

  1. Declaring ** as private** (data hiding).
  2. Providing **public getter and setter methods** to access and modify the fields.


 **Key Points**

1. **Data Hiding** – Fields are kept private, restricting direct external access.
2. **Controlled Access** – Public methods (`getters` and `setters`) control how data is accessed or updated.
3. **Improved Security** – Sensitive data is protected from unauthorized modification.
4. **Flexibility** – You can add validation or custom logic inside getters/setters.
5. **Reusability and Maintainability** – Encapsulation makes code modular and easier to modify.

 **Syntax**

class ClassName {
    // private fields
    private int data;

    // getter
    public int getData() {
        return data;
    }

    // setter
    public void setData(int data) {
        this.data = data;
    }
}


 

    // Getter for age
    public int getAge() {
        return age;
    }

    // Setter for age with validation
    public void setAge(int age) {
        if (age > 0) {
            this.age = age;
        } else {
            System.out.println("Age must be positive!");
        }
    }
}

public class EncapsulationDemo {
    public static void main(String[] args) {
        Student s1 = new Student();

        // Setting values using setter
        s1.setName("Alice");
        s1.setAge(20);

        // Getting values using getter
        System.out.println("Name: " + s1.getName());
        System.out.println("Age: " + s1.getAge());

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
* Access is controlled via `getters` and `setters`.


**Advantages of Encapsulation**

1. **Data Security** – Prevents unauthorized or accidental changes to fields.
2. **Flexibility** – Internal implementation can change without affecting external code.
3. **Validation Control** – Data can be checked before assigning values (e.g., age cannot be negative).
4. **Code Reusability** – Encapsulated classes can be reused across projects.
5. **Maintenance** – Code is modular and easy to maintain.


 **Disadvantages of Encapsulation**

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

