
In Java, arrays allow you to store multiple values of the same data type, and to work effectively with them, we perform 
several important operations such as traversing, inserting, deleting, searching, sorting, and updating. Let’s understand
each of these operations clearly with proper examples.

**1. Traversing an Array:**

Traversing means visiting every element of an array one by one, usually to display or process them. This can be done using a
simple `for` loop or an enhanced `for-each` loop. For example-

class TraverseExample {
    public static void main(String[] args) 
    {
        int[] numbers = {10, 20, 30, 40, 50};
        System.out.println("Array elements are:");
        for (int i = 0; i < numbers.length; i++) 
        {
            System.out.println(numbers[i]);
        }
    }
}

Here, each element of the array is accessed using its index and printed.

**2. Insertion in an Array:**

Since arrays in Java have a fixed size, you cannot directly add a new element once the array is created. To insert a new 
element, you usually create a new array with one extra space and copy elements, adding the new one at the desired position.

class InsertExample 
{
    public static void main(String[] args) 
    {
        int[] arr = {10, 20, 30, 40};
        int newElement = 25;
        int position = 2; // insert at index 2
        int[] newArr = new int[arr.length + 1];
        for (int i = 0, j = 0; i < newArr.length; i++) 
        {
            if (i == position) 
            {
                newArr[i] = newElement;
            } else 
            {
                newArr[i] = arr[j];
                j++;
            }
        }
        System.out.println("Array after insertion:");
        for (int num : newArr) 
        {
            System.out.print(num + " ");
        }
    }
}

This program creates a new array with the element `25` inserted at index 2.

**3. Deletion in an Array:**

Deleting an element from an array means removing a value at a specific index. Because array size is fixed, this is done by
creating a new array that skips the element to be deleted.

class DeleteExample 
{
    public static void main(String[] args) 
    {
        int[] arr = {10, 20, 30, 40, 50};
        int deleteIndex = 2; // remove element at index 2
        int[] newArr = new int[arr.length - 1];
        for (int i = 0, j = 0; i < arr.length; i++) 
        {
            if (i != deleteIndex) 
            {
                newArr[j++] = arr[i];
            }
        }
        System.out.println("Array after deletion:");
        for (int num : newArr) 
        {
            System.out.print(num + " ");
        }
    }
}

Here, the element at index 2 (which is `30`) is removed and a new array without that element is created.

**4. Searching in an Array:**

Searching means finding the position (index) of a specific element in an array. The simplest method is **linear search**, 
where each element is checked one by one.


class SearchExample 
{
    public static void main(String[] args) 
    {
        int[] arr = {10, 20, 30, 40, 50};
        int key = 30;
        boolean found = false;
        for (int i = 0; i < arr.length; i++) 
        {
            if (arr[i] == key) 
            {
                System.out.println("Element found at index: " + i);
                found = true;
                break;
            }
        }
        if (!found) 
        {
            System.out.println("Element not found.");
        }
    }
}

In this example, the program searches for `30` and prints its index if found.

**5. Sorting an Array:**

Sorting means arranging the elements of an array in a particular order, usually ascending or descending. Java provides a 
built-in method `Arrays.sort()` to make sorting simple.

import java.util.Arrays;

class SortExample 
{
    public static void main(String[] args) 
    {
        int[] arr = {50, 10, 30, 20, 40};
        Arrays.sort(arr); // Sort in ascending order
        System.out.println("Array after sorting:");
        for (int num : arr) 
        {
            System.out.print(num + " ");
        }
    }
}

This code arranges the numbers in ascending order using Java’s `Arrays.sort()` method from the `java.util` package.

**6. Updating an Array Element:**

Updating means changing the value of an element at a specific index. This is a simple operation since arrays allow direct 
access by index.

class UpdateExample 
{
    public static void main(String[] args) 
    {
        int[] arr = {10, 20, 30, 40};
        arr[2] = 99; // change value at index 2
        System.out.println("Array after updating:");
        for (int num : arr) 
        {
            System.out.print(num + " ");
        }
    }
}

Here, the element at index 2 is updated from `30` to `99`.

These operations — traversing, inserting, deleting, searching, sorting, and updating — cover the most essential ways of 
working with arrays in Java. They help in efficiently managing data collections, performing computations, and preparing data 
for further processing in programs.
