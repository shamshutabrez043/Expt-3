# Expt-3a
```java

class Student {

    String name;
    int age;
    int marks;

    Student() {
        name = "Not Assigned";
        age = 0;
        marks = 0;
    }

       Student(String n, int a) {
        name = n;
        age = a;
        marks = 0;
    }
 Student(String n, int a, int m) {
        name = n;
        age = a;
        marks = m;
    }

        void display() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
        System.out.println("Marks: " + marks);
    }
public static void main(String[] args) {

        Student s1 = new Student();
        Student s2 = new Student("Alice", 20);
       Student s3 = new Student("Bob", 22, 90);
        s1.display();
        s2.display();
        s3.display();
    }
}
```

output:
![output of 3a](3aoutput.png)

# Expt-3b
```java
import java.util.Arrays;

class BinarySearchDemo {

    public static void main(String[] args) {

        int[] arr = {12, 45, 2, 7, 19, 34, 5};
        int key1 = 19;
        int key2 = 20;

        System.out.print("Elements: ");
        for (int x : arr) {
            System.out.print(x + " ");
        }
        System.out.println();

        System.out.println("Element to search: " + key1);


        Arrays.sort(arr);

        System.out.println("After sorting, the array becomes:");
        for (int x : arr) {
            System.out.print(x + " ");
        }
        System.out.println();

        int pos1 = binarySearch(arr, key1);
        if (pos1 != -1) {
            System.out.println("Element " + key1 + " found at position " + pos1);
        } else {
            System.out.println("Element " + key1 + " not found in the list");
        }


        int pos2 = binarySearch(arr, key2);
        if (pos2 != -1) {
            System.out.println("Element " + key2 + " found at position " + pos2);
        } else {
            System.out.println("Element " + key2 + " not found in the list");
        }
    }


    static int binarySearch(int[] arr, int key) {
        int low = 0, high = arr.length - 1;

        while (low <= high) {
            int mid = (low + high) / 2;

            if (arr[mid] == key)
                return mid + 1; 
            else if (arr[mid] < key)
                low = mid + 1;
            else
                high = mid - 1;
        }
        return -1;
    }
}
```
# output:
![output of 3b](3boutput.png)

# Expt-3c
```java
class BubbleSort {

    public static void main(String[] args) {

        int[] arr = {34, 12, 45, 7, 19};
        int n = arr.length;

        System.out.println("Number of elements: " + n);

        System.out.print("Elements: ");
        for (int i = 0; i < n; i++) {
            System.out.print(arr[i] + " ");
        }
        System.out.println();

        for (int i = 0; i < n - 1; i++) {
            for (int j = 0; j < n - 1 - i; j++) {
                if (arr[j] > arr[j + 1]) {
                    int temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                }
            }
        }

        System.out.println("Expected Output (Sorted Array):");
        for (int i = 0; i < n; i++) {
            System.out.print(arr[i] + " ");
        }
    }
}
```
# output:
![output of 3c](3coutput.png)


