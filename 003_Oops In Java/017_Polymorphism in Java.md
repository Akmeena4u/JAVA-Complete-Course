### Polymorphism in Java

1. Polymorphism is one of the four fundamental principles of Object-Oriented Programming (OOP), along with encapsulation, inheritance, and abstraction. Polymorphism allows objects to be treated as instances of their parent class rather than their actual class
2. Polymorphism allows us to perform a single action in different ways. In other words, polymorphism allows you to define one interface and have multiple implementations. The word "poly" means many and "morphs" means forms, So it means many forms. There are two types of Polymorphisms.
3.  There are two main types of polymorphism in Java:

1. **Compile-time Polymorphism (Static Polymorphism)**
2. **Runtime Polymorphism (Dynamic Polymorphism)**

#### 1. Compile-time Polymorphism

Compile-time polymorphism is achieved through method overloading. It is called compile-time polymorphism because the method to be called is determined at compile time.

**Method Overloading:**

Method overloading occurs when multiple methods have the same name but different parameters within the same class.

Example:
```java
public class CompileTimePolymorphism {
    public void display(int a) {
        System.out.println("Argument: " + a);
    }

    public void display(String a) {
        System.out.println("Argument: " + a);
    }

    public static void main(String[] args) {
        CompileTimePolymorphism obj = new CompileTimePolymorphism();
        obj.display(10);
        obj.display("Hello");
    }
}
```
Output:
```
Argument: 10
Argument: Hello
```

#### 2. Runtime Polymorphism

Runtime polymorphism is achieved through method overriding. It is called runtime polymorphism because the method to be called is determined at runtime.

**Method Overriding:**

Method overriding occurs when a subclass provides a specific implementation of a method that is already defined in its superclass.

Example:
```java
class Animal {
    void sound() {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

class Cat extends Animal {
    @Override
    void sound() {
        System.out.println("Cat meows");
    }
}

public class RuntimePolymorphism {
    public static void main(String[] args) {
        Animal myDog = new Dog();
        Animal myCat = new Cat();

        myDog.sound();
        myCat.sound();
    }
}
```
Output:
```
Dog barks
Cat meows
```

### Key Points about Polymorphism

1. **Dynamic Method Dispatch:** 
   Runtime polymorphism uses dynamic method dispatch, where the call to an overridden method is resolved at runtime rather than compile time.

2. **Code Reusability:**
   Polymorphism enhances code reusability and readability by allowing the same method to be used for different types of objects.

3. **Method Overloading and Overriding:**
   - **Method Overloading:** Same method name with different parameters.
   - **Method Overriding:** Subclass provides a specific implementation of a method already defined in the superclass.

4. **Interfaces and Abstract Classes:**
   Polymorphism is often used in conjunction with interfaces and abstract classes to define methods that must be implemented by subclasses.

### Advantages of Polymorphism

1. **Flexibility:**
   Allows for implementing new functionalities without changing the existing code, providing greater flexibility.

2. **Maintainability:**
   Simplifies code maintenance and reduces the chance of errors by using the same method name for similar functionalities.

3. **Extensibility:**
   Facilitates the addition of new classes and methods without altering the existing framework, thus making the system extensible.

### Example with Abstract Classes and Interfaces

Polymorphism can also be demonstrated using abstract classes and interfaces.

**Abstract Class Example:**
```java
abstract class Shape {
    abstract void draw();
}

class Circle extends Shape {
    @Override
    void draw() {
        System.out.println("Drawing Circle");
    }
}

class Rectangle extends Shape {
    @Override
    void draw() {
        System.out.println("Drawing Rectangle");
    }
}

public class TestPolymorphism {
    public static void main(String[] args) {
        Shape s1 = new Circle();
        Shape s2 = new Rectangle();

        s1.draw();
        s2.draw();
    }
}
```
Output:
```
Drawing Circle
Drawing Rectangle
```

**Interface Example:**
```java
interface Animal {
    void sound();
}

class Dog implements Animal {
    @Override
    public void sound() {
        System.out.println("Dog barks");
    }
}

class Cat implements Animal {
    @Override
    public void sound() {
        System.out.println("Cat meows");
    }
}

public class TestPolymorphism {
    public static void main(String[] args) {
        Animal a1 = new Dog();
        Animal a2 = new Cat();

        a1.sound();
        a2.sound();
    }
}
```
Output:
```
Dog barks
Cat meows
```

### Summary

Polymorphism in Java is a powerful feature that allows methods to perform differently based on the object that invokes them. It can be achieved through method overloading (compile-time polymorphism) and method overriding (runtime polymorphism). By leveraging polymorphism, you can write flexible, maintainable, and extensible code that can easily adapt to new requirements and functionalities.
