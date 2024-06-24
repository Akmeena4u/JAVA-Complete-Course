
### 1 Throw and Throws

**Throws Keyword:**

1. **Declaration:**
   - Declares that a method may throw one or more exceptions.
   - Used in the method signature to indicate that the method might throw exceptions of specified types.
   - Requires the calling method to handle or further declare the exception.

**Example:**
```java
import java.io.IOException;

public class ThrowsExample {
    public static void main(String[] args) throws IOException {
        readFile();
    }

    public static void readFile() throws IOException {
        throw new IOException("File reading error");
    }
}
```
Output:
```
Exception in thread "main" java.io.IOException: File reading error
```

**Throw Keyword:**

1. **Explicit Throw:**
   - Used to explicitly throw an exception from any method or block of code.
   - You can throw either a new instance of an exception or an existing exception object using `throw`.

**Example:**
```java
public class ThrowExample {
    public static void main(String[] args) {
        int a = 10, b = 0;
        if (b == 0) {
            throw new ArithmeticException("Division by zero");
        } else {
            int result = a / b;
            System.out.println("Result: " + result);
        }
    }
}
```
Output:
```
Exception in thread "main" java.lang.ArithmeticException: Division by zero
```
---

###  Finally Block

1. **Execution:**
   - Executes code after the try-catch blocks, used mainly for cleanup operations.
   - Always runs regardless of whether an exception is thrown or caught in the try-catch blocks.
   - Ideal for closing resources like files or database connections to prevent resource leaks.

**Example:**
```java
public class FinallyExample {
    public static void main(String[] args) {
        try {
            int a = 10, b = 0;
            int result = a / b;
        } catch (ArithmeticException e) {
            System.out.println("Exception caught: Division by zero.");
        } finally {
            System.out.println("This block always executes.");
        }
    }
}
```
Output:
```
Exception caught: Division by zero.
This block always executes.
```

