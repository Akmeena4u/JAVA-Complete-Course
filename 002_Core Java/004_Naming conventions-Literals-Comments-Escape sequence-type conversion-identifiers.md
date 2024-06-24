

### 3.1 Naming Conventions
- **camelCase**:
  - Start with a lowercase letter.
  - Capitalize the first letter of each subsequent word.
  - Example: `myVariableName`.
- **snake_case**:
  - Start with a lowercase letter.
  - Separate words with underscores.
  - Example: `my_variable_name`.
- **kebab-case**:
  - All lowercase letters.
  - Separate words with hyphens.
  - Example: `my-variable-name`.
- **Best Practices**:
  - Choose names that are descriptive but not too long.
  - Example: `age`, `firstName`, `isMarried`.

---

### 3.2 Literals
- **Definition**: Fixed values assigned to variables.
- **Types**:
  - **Integer Literals**:
    - Decimal: `int num = 100;`.
    - Hexadecimal: `int hexNum = 0x64;`.
    - Octal: `int octNum = 0144;`.
    - Binary: `int binNum = 0b1100100;`.
  - **Floating-point Literals**:
    - `double pi = 3.14;`.
    - Scientific notation: `double exp = 2.71e2;`.
  - **Character Literals**:
    - `char letter = 'A';`.
    - Escape sequences: `char newline = '\n';`.
  - **String Literals**:
    - `String name = "John";`.
  - **Boolean Literals**:
    - `boolean isTrue = true;`.
    - `boolean isFalse = false;`.

---

### 3.3 Keywords
- **Definition**: Reserved words in Java that have a specific meaning and cannot be used as variable names.
- **Examples**: `class`, `public`, `static`, `void`, `int`, `if`, `else`, `for`, `while`, `return`, `new`, `try`, `catch`, `finally`, `throws`.
- ![image](https://github.com/Akmeena4u/JAVA-Complete-Course/assets/93425334/bfd0cc87-43e8-4a92-966b-25eb9695caa5)

---

### 3.4 Escape Sequences
- **Definition**: Special characters used in strings to represent certain whitespace or other characters.
- **Examples**:
  - `\n`: Newline
  - `\t`: Tab
  - `\\`: Backslash
  - `\"`: Double quote
  - `\'`: Single quote
  - ![image](https://github.com/Akmeena4u/JAVA-Complete-Course/assets/93425334/6a9fbfe5-8efe-44e4-978b-a409efd29e49)

---

### 3.5 Java Comments

### Introduction
- **Comments** in Java are used to explain the code, making it more readable and maintainable.
- Comments are ignored by the Java compiler and do not affect the execution of the program.

### Types of Comments
Java supports three types of comments:
1. **Single-line comments**
2. **Multi-line comments**
3. **Documentation comments**

### 1. Single-line Comments
- Used for brief explanations or notes.
- Syntax: `// comment text`
- **Example**:
  ```java
  // This is a single-line comment
  int age = 25; // Variable to store age
  ```

### 2. Multi-line Comments
- Used for longer comments that span multiple lines.
- Syntax: `/* comment text */`
- **Example**:
  ```java
  /* This is a multi-line comment.
     It can span multiple lines.
     Useful for longer explanations. */
  int sum = a + b;
  ```

### 3. Documentation Comments
- Used to generate external documentation using the Javadoc tool.
- Syntax: `/** comment text */`
- **Example**:
  ```java
  /**
   * This is a documentation comment.
   * It provides detailed information about the code.
   * It can be used by the Javadoc tool to generate HTML documentation.
   */
  public class MyClass {
      /**
       * This method adds two numbers.
       * @param a the first number
       * @param b the second number
       * @return the sum of a and b
       */
      public int add(int a, int b) {
          return a + b;
      }
  }
  ```


### Generating Documentation with Javadoc
- **Javadoc** is a tool provided by Java to generate HTML documentation from documentation comments in the source code.
- **Command**: Run `javadoc MyClass.java` in the terminal to generate HTML documentation for `MyClass.java`.
- The Javadoc tool parses the documentation comments (`/** ... */`) and generates a comprehensive HTML documentation that can be viewed in a web browser.

### Conclusion
Comments play a crucial role in making the code understandable and maintainable. By using single-line, multi-line, and documentation comments appropriately, developers can ensure that their code is well-documented, making it easier for others (and themselves) to understand and maintain the code in the future.

---

### 3.6 Type Conversion and Casting
- **Type Conversion**: Converting a value from one data type to another.
  - **Automatic Type Conversion (Widening)**: Done automatically by the compiler when converting a smaller data type to a larger data type.
    ```java
    int num = 10;
    double doubleNum = num; // int to double
    ```
  - **Manual Type Conversion (Narrowing)**: Requires explicit casting when converting a larger data type to a smaller data type.
    ```java
    double doubleNum = 10.5;
    int num = (int) doubleNum; // double to int
    ```

    ![image](https://github.com/Akmeena4u/JAVA-Complete-Course/assets/93425334/9b40faf3-5edf-4d72-b9a7-37e04836ca7c)

---


### 3.7 Java Identifier Rules
- Allowed characters: `[A-Z]`, `[a-z]`, `[0-9]`, `$` (dollar sign), `_` (underscore).
- Cannot use keywords or reserved words.
- Identifiers should not start with digits `[0-9]`.
- Java identifiers are case-sensitive.
- No limit on the length of the identifier, but use an optimum length of 4 – 15 letters.
