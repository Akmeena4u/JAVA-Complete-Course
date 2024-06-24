## Java Strings

### 1. **What is a Java String?**
   - In Java, a String is a sequence of characters. It's a reference type, which means it's an object that can be manipulated and accessed through various methods.
   - Strings in Java are immutable, meaning their values cannot be changed once they are created. Any operation that seems to modify a string actually creates a new string object.

### 2. **Creating Strings**
   - You can create a string in Java using either a string literal or the `String` class constructor.
     ```java
     String str1 = "Hello"; // Using string literal
     String str2 = new String("World"); // Using String class constructor
     ```

### 3. **String Concatenation**
   - Java provides the `+` operator for string concatenation, which joins two strings into one.
     ```java
     String fullName = "John" + " " + "Doe"; // fullName is "John Doe"
     ```

### 4. **String Methods in Java**

1. **`length()`:** Returns the length of the string.
    ```java
    String str = "Hello, World!";
    int length = str.length(); // length is 13
    ```

2. **`charAt(int index)`:** Returns the character at the specified index.
    ```java
    String str = "Hello";
    char character = str.charAt(2); // character is 'l'
    ```

3. **`substring(int beginIndex)`:** Returns a substring starting from the specified index.
    ```java
    String str = "Hello, World!";
    String substring = str.substring(7); // substring is "World!"
    ```

4. **`substring(int beginIndex, int endIndex)`:** Returns a substring within the specified range.
    ```java
    String str = "Hello, World!";
    String substring = str.substring(7, 12); // substring is "World"
    ```

5. **`toUpperCase()`:** Converts the string to uppercase.
    ```java
    String str = "hello";
    String upperCaseStr = str.toUpperCase(); // upperCaseStr is "HELLO"
    ```

6. **`toLowerCase()`:** Converts the string to lowercase.
    ```java
    String str = "HELLO";
    String lowerCaseStr = str.toLowerCase(); // lowerCaseStr is "hello"
    ```

7. **`indexOf(String str)`:** Returns the index of the first occurrence of a specified substring.
    ```java
    String str = "Hello, World!";
    int index = str.indexOf("World"); // index is 7
    ```

8. **`startsWith(String prefix)`:** Checks if the string starts with a specified prefix.
    ```java
    String str = "Hello, World!";
    boolean startsWithHello = str.startsWith("Hello"); // startsWithHello is true
    ```

9. **`endsWith(String suffix)`:** Checks if the string ends with a specified suffix.
    ```java
    String str = "Hello, World!";
    boolean endsWithWorld = str.endsWith("World!"); // endsWithWorld is true
    ```

10. **`replace(char oldChar, char newChar)`:** Replaces occurrences of a character with another character.
    ```java
    String str = "Hello, World!";
    String replacedStr = str.replace('o', 'x'); // replacedStr is "Hellx, Wxrld!"
    ```

11. **`replaceAll(String regex, String replacement)`:** Replaces substrings that match a regular expression with a specified string.
    ```java
    String str = "Hello, Java!";
    String replacedStr = str.replaceAll("[aeiou]", "*"); // replacedStr is "H*ll*, J*v*!"
    ```

12. **`split(String regex)`:** Splits the string into an array of substrings based on a delimiter.
    ```java
    String str = "Hello,World,Java";
    String[] parts = str.split(","); // parts is {"Hello", "World", "Java"}
    ```

13. **`trim()`:** Removes leading and trailing whitespace from the string.
    ```java
    String str = "   Hello, World!   ";
    String trimmedStr = str.trim(); // trimmedStr is "Hello, World!"
    ```

14. **`equals(Object obj)`:** Checks if the string is equal to another object.
    ```java
    String str1 = "Hello";
    String str2 = new String("Hello");
    boolean isEqual = str1.equals(str2); // isEqual is true
    ```

15. **`compareTo(String anotherString)`:** Compares strings lexicographically.
    ```java
    String str1 = "Hello";
    String str2 = "World";
    int result = str1.compareTo(str2); // result is negative because "Hello" comes before "World"
    ```

### 5. **String Formatting**
   - Java provides the `String.format()` method and `printf()` method for string formatting, allowing you to create formatted strings with placeholders.
     ```java
     String formattedString = String.format("Hello, %s! You are %d years old.", "Alice", 30);
     System.out.println(formattedString); // Output: Hello, Alice! You are 30 years old.
     ```

### 6. **StringBuilder and StringBuffer**
   - When you need to perform a lot of string manipulations, it's better to use `StringBuilder` (or `StringBuffer` for thread-safe operations) due to their mutable nature. They provide methods like `append()`, `insert()`, `delete()`, and `reverse()` for efficient string modifications.

### 7. **String Comparison**
   - In Java, you should use the `equals()` method to compare string contents, as `==` checks for reference equality (whether two variables refer to the same object in memory).
     ```java
     String str1 = "Hello";
     String str2 = new String("Hello");
     boolean isEqual = str1.equals(str2); // isEqual is true
     ```

### 8. **String Interning**
   - Java maintains a string pool where literal strings are stored. Strings created using string literals are interned, meaning they are stored in the pool. This can optimize memory usage when multiple variables reference the same string literal.

### 9. **String Performance**
   - Since strings are immutable, operations like concatenation create new string objects, which can impact performance if done extensively. Using `StringBuilder` or `StringBuffer` for frequent string modifications is more efficient.
