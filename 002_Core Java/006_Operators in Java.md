## 4. Operators in JAVA
Operators in Java are special symbols that perform specific operations on one, two, or three operands, and then return a result. Operators are used to perform various tasks, such as arithmetic calculations, comparisons, logical operations, and more.

---
### 4.1 Assignment Operator

- **Purpose**: Assigns the value of the right-hand operand to the left-hand operand.
- **Syntax**: `variable = value;`
- **Example**: `int a = 5;` assigns the value 5 to the variable `a`.

#### Example: Swapping Two Numbers
```java
int a = 5;
int b = 10;
int temp;

temp = a;
a = b;
b = temp;

System.out.println("a = " + a + ", b = " + b);
```

---

### 4.2 Arithmetic Operators

Arithmetic operators are used to perform basic mathematical operations:

- `+` (Addition)
- `-` (Subtraction)
- `*` (Multiplication)
- `/` (Division)
- `%` (Modulus)

#### Example: Arithmetic Operations
```java
int a = 10;
int b = 5;

System.out.println("Addition: " + (a + b));
System.out.println("Subtraction: " + (a - b));
System.out.println("Multiplication: " + (a * b));
System.out.println("Division: " + (a / b));
System.out.println("Modulus: " + (a % b));
```

---

### 4.3 Order of Operation

Java follows the standard mathematical order of operations, also known as PEMDAS (Parentheses, Exponents, Multiplication and Division, Addition and Subtraction).

---

### 4.4 Shorthand Arthematic Operators

Shorthand operators are a concise way to perform operations and assign values simultaneously:

- `+=` (Addition assignment)
- `-=` (Subtraction assignment)
- `*=` (Multiplication assignment)
- `/=` (Division assignment)
- `%=` (Modulus assignment)

#### Example: Shorthand Operators
```java
int a = 10;
a += 5;  // a = a + 5
System.out.println("a = " + a);  // Output: a = 15
```

---

### 4.5 Unary Arthematic Operators

Unary operators operate on a single operand:

- `+` (Unary plus)
- `-` (Unary minus)
- `++` (Increment)
- `--` (Decrement)
- `!` (Logical complement)

#### Example: Unary Operators
```java
int a = 10;
int b = -a; // Unary minus
System.out.println("b = " + b);  // Output: b = -10

a++;
System.out.println("a = " + a);  // Output: a = 11
```

---

### 4.6 Relational Operators

Relational operators compare two values and return a boolean result:

- `==` (Equal to)
- `!=` (Not equal to)
- `>` (Greater than)
- `<` (Less than)
- `>=` (Greater than or equal to)
- `<=` (Less than or equal to)

#### Example: Relational Operators
```java
int a = 10;
int b = 5;

System.out.println("a == b: " + (a == b));  // Output: false
System.out.println("a != b: " + (a != b));  // Output: true
System.out.println("a > b: " + (a > b));    // Output: true
System.out.println("a < b: " + (a < b));    // Output: false
```
---

### 4.7 Logical Operators

Logical operators are used to combine multiple boolean expressions:

- `&&` (Logical AND)
- `||` (Logical OR)
- `!` (Logical NOT)

#### Example: Logical Operators
```java
boolean a = true;
boolean b = false;

System.out.println("a && b: " + (a && b));  // Output: false
System.out.println("a || b: " + (a || b));  // Output: true
System.out.println("!a: " + (!a));          // Output: false
```
---

### 4.8 Introduction to Bitwise Operators

Bitwise operators perform operations on individual bits of integer values:

- `&` (Bitwise AND)
- `|` (Bitwise OR)
- `^` (Bitwise XOR)
- `~` (Bitwise NOT)
- `<<` (Left shift)
- `>>` (Right shift)
- `>>>` (Unsigned right shift)

#### Example: Bitwise Operators
```java
int a = 5;  // Binary: 0101
int b = 3;  // Binary: 0011

System.out.println("a & b: " + (a & b));  // Output: 1  (Binary: 0001)
System.out.println("a | b: " + (a | b));  // Output: 7  (Binary: 0111)
System.out.println("a ^ b: " + (a ^ b));  // Output: 6  (Binary: 0110)
System.out.println("~a: " + (~a));        // Output: -6 (Binary: 1010)
System.out.println("a << 1: " + (a << 1));  // Output: 10 (Binary: 1010)
System.out.println("a >> 1: " + (a >> 1));  // Output: 2  (Binary: 0010)
System.out.println("a >>> 1: " + (a >>> 1));  // Output: 2  (Binary: 0010)
```
---

### 4.9 Ternary Operator

The ternary operator in Java is a shorthand for the `if-else` statement. It's used to make a quick decision between two values based on a condition. It is also known as the conditional operator.

#### Syntax
```java
condition ? expression1 : expression2;
```

- **condition**: A boolean expression that evaluates to true or false.
- **expression1**: The value that gets returned if the condition is true.
- **expression2**: The value that gets returned if the condition is false.

#### Example: Ternary Operator
```java
int a = 10;
int b = 20;

int max = (a > b) ? a : b;
System.out.println("The maximum value is " + max);  // Output: The maximum value is 20
```

---

### 4.10 Increment and Decrement Operators

Increment and decrement operators are unary operators that add or subtract 1 from a variable.

#### Types
- **Increment Operator (`++`)**
- **Decrement Operator (`--`)**

#### Increment Operator
- **Prefix Increment (`++variable`)**: Increases the value of the variable by 1 before it is used in an expression.
- **Postfix Increment (`variable++`)**: Increases the value of the variable by 1 after it is used in an expression.

#### Example: Prefix Increment
```java
int a = 10;
int b = ++a;  // a is incremented to 11, then b is assigned the value of a

System.out.println("a = " + a);  // Output: a = 11
System.out.println("b = " + b);  // Output: b = 11
```


#### Decrement Operator
- **Prefix Decrement (`--variable`)**: Decreases the value of the variable by 1 before it is used in an expression.
- **Postfix Decrement (`variable--`)**: Decreases the value of the variable by 1 after it is used in an expression.


#### Example: Postfix Decrement
```java
int a = 10;
int b = a--;  // b is assigned the value of a (10), then a is decremented to 9

System.out.println("a = " + a);  // Output: a = 9
System.out.println("b = " + b);  // Output: b = 10
```
---

### 4.11 Operator Precedence

Operator precedence determines the order in which operators are evaluated. Operators with higher precedence are evaluated before operators with lower precedence.

#### Example: Operator Precedence
```java
int result = 10 + 5 * 2;  // Multiplication (*) has higher precedence than addition (+)
System.out.println("Result: " + result);  // Output: Result: 20
```

By understanding these operators and how to use them, you can perform a variety of tasks in Java more efficiently. Practice writing programs that utilize these concepts to become proficient in Java programming.
