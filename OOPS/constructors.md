
**Definition:**

A **constructor** in Java is a special method that is used to *initialize objects*. It is automatically called when an
object of a class is created. Constructors have the same name as the class and do not have a return type.

---

**Why Constructors Are Used:**

• To initialize object data  
• To assign default values to variables  
• To perform setup tasks during object creation  
• To ensure objects start in a valid state  

---

**Key Characteristics of Constructors:**

• Constructor name must be the same as the class name  
• Constructors do not have a return type (not even void)  
• Constructors are called automatically when an object is created  
• A class can have multiple constructors  

---

**1. Default Constructor -**

A **default constructor** is a constructor that takes *no parameters*. If no constructor is defined, Java provides one
automatically.

Example:

class Student
{
    Student()
    {
        System.out.println("Default constructor called");
    }

    public static void main(String[] args)
    {
        Student s = new Student();
    }
}

**Output:**

Default constructor called

---

**2. Parameterized Constructor -**

A **parameterized constructor** accepts parameters and initializes the object with provided values.

Example:

class Student
{
    int id;
    String name;

    Student(int i, String n)
    {
        id = i;
        name = n;
    }

    void display()
    {
        System.out.println(id + " " + name);
    }

    public static void main(String[] args)
    {
        Student s1 = new Student(101, "Aman");
        Student s2 = new Student(102, "Riya");

        s1.display();
        s2.display();
    }
}

**Output:**

101 Aman  
102 Riya  

---

**3. Constructor Overloading -**

When a class has more than one constructor with different parameters, it is called constructor overloading.

Example:

class Product
{
    int id;
    String name;

    Product()
    {
        id = 0;
        name = "Unknown";
    }

    Product(int i, String n)
    {
        id = i;
        name = n;
    }

    void show()
    {
        System.out.println(id + " " + name);
    }

    public static void main(String[] args)
    {
        Product p1 = new Product();
        Product p2 = new Product(201, "Laptop");

        p1.show();
        p2.show();
    }
}

**Output:**

0 Unknown  
201 Laptop  

---

**4. Copy Constructor (Concept) -**

Java does not provide a built-in copy constructor, but it can be created manually to copy values from another object.

Example:

class Book
{
    String title;

    Book(String t)
    {
        title = t;
    }

    Book(Book b)
    {
        title = b.title;
    }

    void display()
    {
        System.out.println(title);
    }

    public static void main(String[] args)
    {
        Book b1 = new Book("Java Programming");
        Book b2 = new Book(b1);

        b1.display();
        b2.display();
    }
}

---

**Important Points to Remember -**

• Constructors initialize objects  
• They are called automatically during object creation  
• Constructors can be overloaded  
• Constructors cannot be static  
• Constructors cannot be inherited  

---

**Difference Between Constructor and Method -**

| Feature        | Constructor             | Method                 |
|---------------|--------------------------|------------------------|
| Name          | Same as class name       | Any valid name         |
| Return type   | No return type           | Has return type        |
| Called by     | Automatically            | Explicitly             |
| Purpose       | Initialize object        | Perform operations     |

---

**Summary:**

• Constructors are special methods used to initialize objects  
• They run automatically when an object is created  
• Java supports default and parameterized constructors  
• Constructor overloading is allowed  
• Constructors are a key part of OOPS
