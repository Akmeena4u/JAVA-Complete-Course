## Taking User Input in Java

In Java, user input can be taken using the `Scanner` class from the `java.util` package. This class provides methods to read different types of inputs such as integers, floating-point numbers, strings, etc.

### Steps to Take User Input

1. **Import the `Scanner` class**.
2. **Create an instance of the `Scanner` class**.
3. **Use the `Scanner` methods to read input**.

### Example Code

Here is a step-by-step guide with examples for reading different types of user inputs in Java:

### 1. Import the `Scanner` Class

Before you can use the `Scanner` class, you need to import it.

```java
import java.util.Scanner;
```

### 2. Create an Instance of the `Scanner` Class

Create an instance of the `Scanner` class and pass `System.in` to it, which tells the `Scanner` to read input from the standard input stream (keyboard).

```java
Scanner scanner = new Scanner(System.in);
```

### 3. Reading Different Types of Inputs

#### Reading a String

To read a string, you can use the `nextLine()` method.

```java
System.out.print("Enter your name: ");
String name = scanner.nextLine();
System.out.println("Welcome, " + name + "!");
```

#### Reading an Integer

To read an integer, use the `nextInt()` method.

```java
System.out.print("Enter your age: ");
int age = scanner.nextInt();
System.out.println("Your age is " + age + ".");
```

#### Reading a Floating-point Number

To read a floating-point number, use the `nextFloat()` method.

```java
System.out.print("Enter your height in meters: ");
float height = scanner.nextFloat();
System.out.println("Your height is " + height + " meters.");
```

#### Reading a Double

To read a double, use the `nextDouble()` method.

```java
System.out.print("Enter the price: ");
double price = scanner.nextDouble();
System.out.println("The price is " + price + ".");
```

### Closing the Scanner

After you are done using the `Scanner`, it's a good practice to close it to free up resources.

```java
scanner.close();
```

### Full Example

Here is a full example that takes different types of inputs from the user:

```java
import java.util.Scanner;

public class UserInputExample {
    public static void main(String[] args) {
        // Create a Scanner object
        Scanner scanner = new Scanner(System.in);
        
        // Reading a string
        System.out.print("Enter your name: ");
        String name = scanner.nextLine();
        System.out.println("Welcome, " + name + "!");
        
        // Reading an integer
        System.out.print("Enter your age: ");
        int age = scanner.nextInt();
        System.out.println("Your age is " + age + ".");
        
        // Reading a float
        System.out.print("Enter your height in meters: ");
        float height = scanner.nextFloat();
        System.out.println("Your height is " + height + " meters.");
        
        // Reading a double
        System.out.print("Enter the price: ");
        double price = scanner.nextDouble();
        System.out.println("The price is " + price + ".");
        
        // Close the scanner
        scanner.close();
    }
}
```

### Handling Exceptions

When taking user input, it's important to handle potential exceptions, especially `InputMismatchException`, which occurs if the user inputs a type that doesn't match the expected type.

#### Example with Exception Handling

```java
import java.util.InputMismatchException;
import java.util.Scanner;

public class SafeUserInputExample {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        try {
            System.out.print("Enter your age: ");
            int age = scanner.nextInt();
            System.out.println("Your age is " + age + ".");
        } catch (InputMismatchException e) {
            System.out.println("Invalid input! Please enter a valid integer.");
        }
        
        scanner.close();
    }
}
```

### Conclusion

Taking user input in Java is straightforward with the `Scanner` class. By understanding the methods available in this class, you can easily read various types of inputs from the user. Remember to handle exceptions to make your program more robust and user-friendly.
