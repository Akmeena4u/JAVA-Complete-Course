
## Conditional Statements

Conditional statements in Java are used to control the flow of execution based on certain conditions. These statements allow you to make decisions in your program by evaluating whether a condition is true or false. There are primarily three types of conditional statements in Java:

1. **if Statement**
2. **if-else Statement**
3. **if-else-if ladder**
4. **switch Statement**

### 1. if Statement

The `if` statement evaluates a condition and executes a block of code only if the condition is true. If the condition is false, the block of code inside the `if` statement is skipped.

```java
if (condition) {
    // Code to be executed if condition is true
}
```

### 2. if-else Statement

The `if-else` statement extends the `if` statement by providing an alternative block of code to execute if the condition is false.

```java
if (condition) {
    // Code to be executed if condition is true
} else {
    // Code to be executed if condition is false
}
```

### 3. if-else-if ladder

The `if-else-if` ladder allows you to evaluate multiple conditions sequentially. It starts with an `if` statement, followed by zero or more `else if` statements, and optionally ends with an `else` statement.

```java
if (condition1) {
    // Code to be executed if condition1 is true
} else if (condition2) {
    // Code to be executed if condition2 is true
} else if (condition3) {
    // Code to be executed if condition3 is true
} else {
    // Code to be executed if none of the conditions are true
}
```

### 4. switch Statement

The `switch` statement is used to select one choice from multiple options based on the value of an expression. It's an alternative to using multiple `if-else-if` statements when dealing with multiple conditions.

```java
switch (expression) {
    case value1:
        // Code to be executed if expression equals value1
        break;
    case value2:
        // Code to be executed if expression equals value2
        break;
    // More cases...
    default:
        // Code to be executed if expression doesn't match any case
}
```

### Examples

#### Example using if Statement

```java
int num = 10;
if (num > 0) {
    System.out.println("Number is positive");
}
```

#### Example using if-else Statement

```java
int num = -5;
if (num > 0) {
    System.out.println("Number is positive");
} else {
    System.out.println("Number is non-positive");
}
```

#### Example using if-else-if ladder

```java
int num = 0;
if (num > 0) {
    System.out.println("Number is positive");
} else if (num < 0) {
    System.out.println("Number is negative");
} else {
    System.out.println("Number is zero");
}
```

#### Example using switch Statement

```java
char grade = 'B';
switch (grade) {
    case 'A':
        System.out.println("Excellent");
        break;
    case 'B':
        System.out.println("Good");
        break;
    case 'C':
        System.out.println("Average");
        break;
    default:
        System.out.println("Invalid grade");
}
```

These conditional statements allow you to create flexible and decision-making logic in your Java programs.
