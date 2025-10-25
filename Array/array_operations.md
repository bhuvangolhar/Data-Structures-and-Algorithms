
**Array Operations :**

• Ar
int pos = 2, element = 25;
for (int i = arr.length - 1; i > pos; i--) 
{
    arr[i] = arr[i - 1];
}
arr[pos] = element;

**Deleting an element :**

• Removing an element from a given position.
• Requires shifting remaining elements to fill the gap.

int arr[] = 
int arr[] = {50, 20, 40, 10};
Arrays.sort(arr);

**Summary of Operations :**

✔ Traverse → Visit each element.
✔ Insert → Add an element (requires shifting).
