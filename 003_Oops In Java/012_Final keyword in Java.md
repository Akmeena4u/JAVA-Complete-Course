
### Final Variable

A final variable is a constant that cannot be changed once initialized. It is typically used for values that should not be modified during the program's execution.

```java
class Bike {
    final int speedlimit = 90; // final variable

    void run() {
        // speedlimit = 400; // Compile-time error: Cannot change final variable
        System.out.println("Speed Limit: " + speedlimit);
    }

    public static void main(String args[]) {
        Bike obj = new Bike();
        obj.run();
    }
}
```

### Final Method

A final method cannot be overridden in subclasses. It ensures that the method's implementation remains constant across all subclasses.

```java
class Bike {
    final void run() {
        System.out.println("running");
    }
}

class Honda extends Bike {
    // void run() { // Compile-time error: Cannot override final method
    //     System.out.println("running safely with 100kmph");
    // }

    public static void main(String args[]) {
        Honda honda = new Honda();
        honda.run();
    }
}
```

### Final Class

A final class cannot be subclassed or extended. It provides a guarantee that no other class can inherit from it.

```java
final class Bike {} // Final class

// class Honda extends Bike { // Compile-time error: Cannot extend final class
//     void run() {
//         System.out.println("running safely with 100kmph");
//     }
// }
```

### Blank Final Variable

A blank final variable is a final variable that is not initialized at declaration. It must be initialized in the constructor.

```java
class Student {
    int id;
    String name;
    final String PAN_CARD_NUMBER; // Blank final variable

    Student(int id, String name, String pan) {
        this.id = id;
        this.name = name;
        this.PAN_CARD_NUMBER = pan; // Initialized in constructor
    }
}
```

### Static Blank Final Variable

A static blank final variable is a static final variable that is not initialized at declaration and is initialized in a static block.

```java
class A {
    static final int data; // Static blank final variable

    static {
        data = 50; // Initialized in static block
    }

    public static void main(String args[]) {
        System.out.println(A.data);
    }
}
```

### Final Parameter

A final parameter in a method ensures that its value cannot be changed within the method.

```java
class Bike {
    int cube(final int n) {
        // n = n + 2; // Compile-time error: Cannot change final parameter
        return n * n * n;
    }

    public static void main(String args[]) {
        Bike b = new Bike();
        System.out.println("Cube of 5: " + b.cube(5));
    }
}
```

The final keyword in Java is versatile, providing immutability and ensuring constant behavior for variables, methods, and classes where it's applied.
