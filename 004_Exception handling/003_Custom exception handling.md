###  Custom Exceptions

1. **Definition:**
   - Custom exceptions are user-defined exception classes that extend either `Exception` (for checked exceptions) or `RuntimeException` (for unchecked exceptions).
   - They are created to represent specific error conditions relevant to an application.

**Example:**
```java
class CustomException extends Exception {
    public CustomException(String message) {
        super(message);
    }
}

public class CustomExceptionExample {
    public static void main(String[] args) {
        try {
            validateAge(15);
        } catch (CustomException e) {
            System.out.println("Exception caught: " + e.getMessage());
        }
    }

    static void validateAge(int age) throws CustomException {
        if (age < 18) {
            throw new CustomException("Age is not valid to vote.");
        } else {
            System.out.println("Welcome to vote.");
        }
    }
}
```
Output:
```
Exception caught: Age is not valid to vote.
```

