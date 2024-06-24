
### 1. Loops in Java

Loops in Java are used to execute a block of code repeatedly as long as a specified condition is true. There are mainly three types of loops in Java:

1. **for loop**
2. **while loop**
3. **do-while loop**

#### 1.1 for Loop

The `for` loop is used when you know exactly how many times you want to execute a block of code. It consists of three parts: initialization, condition, and increment/decrement.

```java
for (initialization; condition; increment/decrement) {
    // code to be executed repeatedly
}
```

Example:

```java
for (int i = 1; i <= 5; i++) {
    System.out.println("Iteration: " + i);
}
```

#### 1.2 while Loop

The `while` loop is used when you want to execute a block of code as long as a condition is true. The condition is evaluated before executing the block of code.

```java
while (condition) {
    // code to be executed repeatedly
}
```

Example:

```java
int i = 1;
while (i <= 5) {
    System.out.println("Iteration: " + i);
    i++;
}
```

#### 1.3 do-while Loop

The `do-while` loop is similar to the `while` loop, but it guarantees that the block of code inside the loop is executed at least once, even if the condition is false.

```java
do {
    // code to be executed repeatedly
} while (condition);
```

Example:

```java
int i = 1;
do {
    System.out.println("Iteration: " + i);
    i++;
} while (i <= 5);
```

### 2. The `continue` Statement

The `continue` statement is used inside loops to skip the remaining code inside the loop for the current iteration and proceed to the next iteration.

Example:

```java
for (int i = 1; i <= 5; i++) {
    if (i == 3) {
        continue; // Skip iteration 3
    }
    System.out.println("Iteration: " + i);
}
```

### 3. The `break` Statement

The `break` statement is used inside loops to terminate the loop immediately and continue with the code outside the loop.

Example:

```java
for (int i = 1; i <= 5; i++) {
    if (i == 3) {
        break; // Exit the loop at iteration 3
    }
    System.out.println("Iteration: " + i);
}
```

These looping constructs along with the `continue` and `break` statements provide powerful control over the flow of execution in Java programs, allowing you to create efficient and flexible logic.
