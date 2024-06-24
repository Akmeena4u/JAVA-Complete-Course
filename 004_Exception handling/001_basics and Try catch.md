### 1 What is an Exception

![image](https://github.com/Akmeena4u/JAVA-Complete-Course/assets/93425334/520c1dd0-23a2-449f-a149-abaf5a1fc57f)


1. **Definition:**
   - In Java, an exception is a disruptive event that occurs during the execution of a program, interrupting its normal flow. Examples include arithmetic errors, null pointer accesses, and resource overflows.
   - Exceptions are objects in Java that encapsulate information about an error event, including its type and the state of the program when the error occurred.

**Example:**
```java
public class ExceptionExample {
    public static void main(String[] args) {
        int a = 10, b = 0;
        try {
            int result = a / b; // This will throw ArithmeticException
        } catch (ArithmeticException e) {
            System.out.println("Exception caught: Division by zero.");
        }
    }
}
```
Output:
```
Exception caught: Division by zero.
```

### 2 Try-Catch


1. **Try Block:**
   - Contains code that is susceptible to exceptions.
   - If an exception occurs in the try block, it is thrown to the catch block.

2. **Catch Block:**
   - Follows the try block and handles the exceptions thrown by the try block.
   - Control is transferred to the catch block when an exception occurs in the try block.

![image](https://github.com/Akmeena4u/JAVA-Complete-Course/assets/93425334/d6a7cb65-b4a6-426b-8539-c01d220265d8)

**Example:**
```java
public class TryCatchExample {
    public static void main(String[] args) {
        try {
            int[] numbers = {1, 2, 3};
            System.out.println(numbers[5]); // This will throw ArrayIndexOutOfBoundsException
        } catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Exception caught: Array index out of bounds.");
        }
    }
}
```
Output:
```
Exception caught: Array index out of bounds.
```

### 3 Types of Exceptions

![image](https://github.com/Akmeena4u/JAVA-Complete-Course/assets/93425334/282dfbe8-54c0-496d-8214-bf8df19bf5c9)


1. **Checked Exceptions:**
   - These exceptions must be either caught or declared in the method.
   - Example: `IOException`, `SQLException`.

2. **Unchecked Exceptions:**
   - These exceptions do not need to be explicitly handled.
   - Example: `ArithmeticException`, `NullPointerException`.

**Example of Checked Exception:**
```java
import java.io.File;
import java.io.FileNotFoundException;
import java.io.FileReader;

public class CheckedExceptionExample {
    public static void main(String[] args) {
        try {
            File file = new File("nonexistentfile.txt");
            FileReader fr = new FileReader(file);
        } catch (FileNotFoundException e) {
            System.out.println("File not found exception caught.");
        }
    }
}
```
Output:
```
File not found exception caught.
```
