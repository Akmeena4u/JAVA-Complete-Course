
## 2.10 First Java Class

### Step-by-Step Guide to Writing Your First Java Program

1. **Open IntelliJ IDEA**:
   - Launch IntelliJ IDEA on your computer.

2. **Create a New Project**:
   - Select "Create New Project".
   - Choose "Java" from the list of project types.
   - Ensure you select the correct JDK version.

3. **Set Up Project SDK**:
   - Point to the JDK you installed earlier.
   - Click "Next" and configure the project settings.

4. **Create a New Java Class**:
   - In the project view, right-click on the `src` directory.
   - Select "New" > "Java Class".
   - Name your class (e.g., `HelloWorld`).

5. **Write the Java Code**:
   - Your class should look like this:
     ```java
     public class HelloWorld {
         public static void main(String[] args) {
             System.out.println("Hello, World!");
         }
     }
     ```

### Explanation of the First Java Program

![image](https://github.com/Akmeena4u/JAVA-Complete-Course/assets/93425334/5cf4f9b4-7710-436b-a80e-96ad04de3cec)


1. **Class Declaration**:
   ```java
   public class HelloWorld {
   ```
   - **public**: An access modifier, allowing the class to be accessible from other classes.
   - **class**: Keyword used to declare a class.
   - **HelloWorld**: The name of the class. Class names should start with an uppercase letter and follow camel case naming convention.

2. **Main Method**:
   ```java
   public static void main(String[] args) {
   ```
   - **public**: Allows the method to be accessible from outside the class.
   - **static**: Allows the method to be called without creating an instance of the class.
   - **void**: Indicates that the method does not return any value.
   - **main**: The name of the method. It's the entry point of any Java application.
   - **String[] args**: A parameter passed to the main method. It represents an array of `String` objects and can store command-line arguments.

3. **Print Statement**:
   ```java
   System.out.println("Hello, World!");
   ```
   - **System**: A class in the `java.lang` package.
   - **out**: A static member of the `System` class, which is an instance of `PrintStream`.
   - **println**: A method of `PrintStream` that prints the argument passed to it and then terminates the line.

4. **Class Closure**:
   ```java
   }
   ```
   - Closes the class definition.

## 2.10 Project Structure

### Understanding the Project Structure in IntelliJ IDEA

1. **Project Root**:
   - The top-level directory of your project. It contains all the files and folders related to your project.

2. **src (Source) Folder**:
   - This folder contains all your Java source files. By convention, all your Java classes are placed inside this folder.
   - Example: `src/HelloWorld.java`.

3. **Out Folder**:
   - This folder is created by IntelliJ IDEA to store the compiled `.class` files. It contains the bytecode that the JVM can execute.

4. **Libraries**:
   - This section includes all the libraries and dependencies required for your project. The JDK will be listed here as well.

5. **External Libraries**:
   - This contains external libraries and dependencies that your project might use. For a basic project, this usually includes the JDK.

### Example Project Structure:

```
MyFirstJavaProject/
├── .idea/
│   ├── ...
├── out/
│   ├── production/
│       ├── MyFirstJavaProject/
│           ├── HelloWorld.class
├── src/
│   ├── HelloWorld.java
├── MyFirstJavaProject.iml
└── README.md
```

- **.idea/**: Contains project-specific settings and configurations.
- **out/**: Contains compiled bytecode files.
- **src/**: Contains source code files.
- **MyFirstJavaProject.iml**: IntelliJ project file.
- **README.md**: A markdown file for project documentation (optional).

### Running Your Java Program

1. **Compile the Program**:
   - IntelliJ IDEA compiles your code automatically.
   - If you need to manually compile, use the `Build` menu and select `Build Project`.

2. **Run the Program**:
   - Right-click on the `HelloWorld` class file.
   - Select `Run 'HelloWorld.main()'`.
   - The output should display "Hello, World!" in the Run window at the bottom of the screen.

### Summary

In this section, you've learned how to set up your first Java project using IntelliJ IDEA, write a simple Java program, and understand the project structure. You also explored the purpose and functionality of each part of the Java program, including the class declaration, main method, and print statement. This foundational knowledge will help you as you delve deeper into Java programming.
