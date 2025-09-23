
**Array Operations :**

• Arrays are one of the most important data structures in Java.
• They allow storing multiple values of the same type in a single variable. 
• To make arrays useful, we perform various operations such as traversing, inserting, deleting, updating, and searching.

**Traversing an array :**

• Traversing means visiting each element of an array one by one.
• Usually done using loops (for, while, for-each).


int arr[] = {10, 20, 30, 40};
int pos = 2, element = 25;
for (int i = arr.length - 1; i > pos; i--) 
{
    arr[i] = arr[i - 1];
}
arr[pos] = element;

**Deleting an element :**

• Removing an element from a given position.
• Requires shifting remaining elements to fill the gap.

int arr[] = {10, 20, 30, 40, 50};
int pos = 2; 
for (int i = pos; i < arr.length - 1; i++) 
{
    arr[i] = arr[i + 1];
}

**Updating an element :**



• Check each element one by one.

int arr[] = {5, 15, 25, 35};
int key = 25;

for (int i = 0; i < arr.length; i++) 
{
    if (arr[i] == key)
    {
        found = true;
        break;
    }
}

**(b)** *Binary Search -*

• Works only on sorted arrays.
• Efficient, O(log n) time complexity.

import java.util.Arrays;

int index = Arrays.binarySearch(arr, 30);

**Sorting the elements :**

• Rearranging elements in ascending/descending order.
• Example: Bubble Sort, Selection Sort, Insertion Sort.

int arr[] = {50, 20, 40, 10};
Arrays.sort(arr);

**Summary of Operations :**

✔ Traverse → Visit each element.
✔ Insert → Add an element (requires shifting).
