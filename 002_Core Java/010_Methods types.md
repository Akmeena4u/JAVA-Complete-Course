## Java Method types
In Java, methods can be categorized into different types based on their functionality and how they are defined. Let's explore the types of methods in Java:

### 1. Predefined Methods

Predefined methods are built-in methods provided by Java libraries or classes. These methods serve common purposes and are readily available for use in your programs. Examples include methods for string manipulation, mathematical operations, input/output handling, and more.

#### Example of Predefined Methods:

```java
public class PredefinedMethodsExample {
    public static void main(String[] args) {
        // Example of a predefined method
        String text = "Hello, World!";
        int length = text.length(); // Using the length() method of String class
        System.out.println("Length of the text: " + length);
    }
}
```

In this example, `length()` is a predefined method of the `String` class used to get the length of a string.

### 2. Derived Methods (User-Defined Methods)

Derived methods, also known as user-defined methods, are created by the programmer to perform specific tasks as needed in the program. These methods enhance code readability, promote code reuse, and help in organizing code into logical units.

#### Example of Derived Methods:

```java
public class DerivedMethodsExample {
    // User-defined method to calculate the square of a number
    public static int calculateSquare(int num) {
        return num * num;
    }

    public static void main(String[] args) {
        int result = calculateSquare(5); // Calling the user-defined method
        System.out.println("Square of 5 is: " + result);
    }
}
```

In this example, `calculateSquare` is a user-defined method that calculates the square of a number.

### 3. Static Methods

Static methods belong to the class rather than an instance of the class. They can be called directly using the class name without creating an object of the class. Static methods are commonly used for utility functions or operations that do not require access to instance variables.

### 4. Instance Methods

Instance methods belong to an instance of a class and can access instance variables and other instance methods. These methods are invoked on objects of the class and are used to perform operations that depend on the object's state.

---


