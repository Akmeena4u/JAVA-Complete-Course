Here are some of the commonly used predefined methods for arrays in Java:

1. **`length`:** Returns the length of the array.
   ```java
   int[] array = {1, 2, 3, 4, 5};
   int length = array.length; // length is 5
   ```

2. **`clone`:** Creates a copy of the array.
   ```java
   int[] array = {1, 2, 3};
   int[] newArray = array.clone(); // newArray is a copy of array
   ```

3. **`copyOf`:** Copies a specified range of elements from the array.
   ```java
   int[] array = {1, 2, 3, 4, 5};
   int[] newArray = Arrays.copyOf(array, 3); // newArray is {1, 2, 3}
   ```

4. **`fill`:** Sets all elements of the array to a specific value.
   ```java
   int[] array = new int[5];
   Arrays.fill(array, 10); // array is {10, 10, 10, 10, 10}
   ```

5. **`sort`:** Sorts the array in ascending order.
   ```java
   int[] array = {5, 3, 1, 4, 2};
   Arrays.sort(array); // array is sorted to {1, 2, 3, 4, 5}
   ```

6. **`binarySearch`:** Searches for a specified element in the sorted array using binary search.
   ```java
   int[] array = {1, 2, 3, 4, 5};
   int index = Arrays.binarySearch(array, 3); // index is 2 (element found)
   ```

7. **`equals`:** Compares two arrays to check if they are equal.
   ```java
   int[] array1 = {1, 2, 3};
   int[] array2 = {1, 2, 3};
   boolean isEqual = Arrays.equals(array1, array2); // isEqual is true
   ```

8. **`asList`:** Converts an array to a List.
   ```java
   String[] array = {"Java", "Python", "C++"};
   List<String> list = Arrays.asList(array); // list contains {"Java", "Python", "C++"}
   ```

9. **`toString`:** Converts the array to a String representation.
   ```java
   int[] array = {1, 2, 3};
   String arrayString = Arrays.toString(array); // arrayString is "[1, 2, 3]"
   ```

10. **`stream`:** Converts the array to a Stream for functional-style operations.
    ```java
    int[] array = {1, 2, 3, 4, 5};
    IntStream stream = Arrays.stream(array); // Stream<Integer> for array elements
    ```

These methods are part of the `java.util.Arrays` class and are handy for performing various operations on arrays in Java.
