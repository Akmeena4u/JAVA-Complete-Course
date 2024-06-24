

## 2. Java Basics


### 2.1 Installing JDK
1. **Search JDK Download**:
   - Use a search engine to look for "JDK Download".
2. **Oracle Website**:
   - Ensure you download the JDK from the official Oracle website.
3. **Download Latest Version**:
   - Download and install the latest version of the JDK suitable for your operating system.

---

### 2.2 First Class using Text Editor
1. **Open Text Editor**:
   - Use any simple text editor like Notepad or Notepad++.
2. **Write a Simple Java Program**:
   - Example:
     ```java
     public class HelloWorld {
         public static void main(String[] args) {
             System.out.println("Hello, World!");
         }
     }
     ```
3. **Save the File**:
   - Save the file with a `.java` extension, e.g., `HelloWorld.java`.

### 2.3 Compiling and Running
1. **Open Command Prompt/Terminal**:
   - Navigate to the directory where your `.java` file is saved.
2. **Compile the Java Program**:
   - Use the command: `javac HelloWorld.java`
   - This will generate a `HelloWorld.class` file.
3. **Run the Java Program**:
   - Use the command: `java HelloWorld`
   - The output should be: `Hello, World!`

![image](https://github.com/Akmeena4u/JAVA-Complete-Course/assets/93425334/3ff445e1-0b1a-40fb-9f58-aad3d89cfec3)


---

### 2.3 JDK vs JVM vs JRE
1. **JDK (Java Development Kit)**:
   - A software development kit required to develop Java applications.
   - Includes JRE, compiler (javac), and other development tools.
   - A superset of JRE.
2. **JRE (Java Runtime Environment)**:
   - Part of JDK and can be downloaded separately.
   - Provides libraries, JVM, and other components to run Java applications.
   - Does not include development tools like compilers or debuggers.
3. **JVM (Java Virtual Machine)**:
   - Part of JRE responsible for executing bytecode.
   - Ensures Java's "write-once, run-anywhere" capability.
   - Platform-specific: different JVMs for different operating systems.

### 2.4 Showing Output
1. **System.out.println**:
   - Used to print output to the console.
   - Example:
     ```java
     System.out.println("Hello, World!");
     ```

### 2.5 Importance of the main method
1. **Entry Point**:
   - The starting point of a Java program.
   - The JVM looks for the `main` method to begin execution.
2. **Public and Static**:
   - The `main` method must be public and static.
   - Public: Accessible to the JVM.
   - Static: Can be called without creating an instance of the class.
3. **Fixed Signature**:
   - The `main` method must have the signature:
     ```java
     public static void main(String[] args)
     ```

---
