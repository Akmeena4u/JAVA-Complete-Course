
### 1.1 What are Functions/Methods?
1. Definition: Methods are blocks of reusable code that perform specific tasks. They follow the "Don't Repeat Yourself" (DRY) principle, encouraging code reusability.
2. Usage: Methods help organize code into manageable chunks and facilitate code reuse, enhancing maintainability and readability.
3. Naming Rules: Method names follow the same conventions as variable names, using camelCase.
4. Example: "Beta Gas band kar de" can be a method that turns off a gas supply.
5. ![image](https://github.com/Akmeena4u/JAVA-Complete-Course/assets/93425334/b0b87ec9-2ee7-4030-be40-a70188f7c0b9)


Here's an example of a simple method in Java:

```java
public class GasUtility {
    // Method to turn off the gas supply
    public void turnOffGas() {
        System.out.println("Gas supply turned off.");
        // Additional logic to turn off the gas goes here
    }

    public static void main(String[] args) {
        GasUtility gasUtil = new GasUtility();
        gasUtil.turnOffGas(); // Calling the method to turn off the gas
    }
}
```

In this code:

- `GasUtility` is a class that contains a method `turnOffGas()` which prints a message indicating that the gas supply is turned off.
- The `main` method is used to create an instance of `GasUtility` and call its `turnOffGas()` method.

---

### 1.2 Method Syntax

1. Naming: Method names follow the same rules as variable names, ensuring readability and adherence to naming conventions.
2. Parameters: Methods can accept input parameters enclosed in parentheses ().
3. Invocation: To use a method, you call its name followed by parentheses, optionally passing arguments.
4. Organization and Reusability: Methods are fundamental for organizing code into modular and reusable components, promoting code efficiency and maintenance.

Here's an example:

```java
public class Example {
    // Method with parameters
    public void greetUser(String name) {
        System.out.println("Hello, " + name + "!");
    }

    public static void main(String[] args) {
        Example ex = new Example();
        ex.greetUser("John"); // Calling the method with an argument
    }
}
```

In this code:

- `Example` is a class that contains a method `greetUser(String name)` which takes a `String` parameter `name` and prints a greeting message.
- The `main` method creates an instance of `Example` and calls its `greetUser` method with the argument `"John"`.

---

### 1.3 Return Statement

1. The `return` statement in Java is used to send a value back from a method.
2. Example: "Ek glass paani laao" could be a method that returns the quantity of water needed.
3. Returnable Values: Methods can return various types of values, such as variables, calculations, or constants.
4. Function Termination: The return statement immediately ends the function's execution, returning control to the caller.

Here's an example:

```java
public class WaterUtility {
    // Method to calculate the quantity of water needed
    public int calculateWaterQuantity(int glassesNeeded) {
        return glassesNeeded * 250; // Assuming each glass is 250ml
    }

    public static void main(String[] args) {
        WaterUtility waterUtil = new WaterUtility();
        int waterAmount = waterUtil.calculateWaterQuantity(3);
        System.out.println("Bring " + waterAmount + "ml of water.");
    }
}
```

In this code:

- `WaterUtility` is a class with a method `calculateWaterQuantity(int glassesNeeded)` that calculates the total quantity of water needed based on the number of glasses required.
- The `main` method calls `calculateWaterQuantity` with an argument of `3` glasses and prints the calculated water amount.

---

### 1.4 Arguments vs Parameters

1. Arguments are input values passed to a method, while parameters are placeholders for these values within the method.
2. Input Values: Arguments are the actual values passed to a method, while parameters are variables that store these values within the method's scope.
3. Parameter Passing: Parameters receive input values, and return sends values back from the method.
4. Example: "Ek packet dahi laao" might be a method where "packet" is a parameter representing the quantity of yogurt.
5. Multiple Parameters: Methods can accept multiple parameters, enabling versatility and customization.
6. Default Values: Parameters can have default values, providing flexibility in method invocation.

Here's an example:

```java
public class YogurtUtility {
    // Method with a parameter
    public void getRequiredYogurt(int packetsNeeded) {
        System.out.println("Bring " + packetsNeeded + " packets of yogurt.");
    }

    public static void main(String[] args) {
        YogurtUtility yogurtUtil = new YogurtUtility();
        yogurtUtil.getRequiredYogurt(2); // Calling the method with an argument
    }
}
```

In this code:

- `YogurtUtility` is a class with a method `getRequiredYogurt(int packetsNeeded)` that expects an `int` parameter indicating the number of yogurt packets needed.
- The `main` method calls `getRequiredYogurt` with an argument of `2` packets.
