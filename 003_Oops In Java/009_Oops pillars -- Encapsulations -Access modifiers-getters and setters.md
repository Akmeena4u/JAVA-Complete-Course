### Introduction to OOPs Principles
Object-Oriented Programming (OOP) is a paradigm based on the concept of objects, which can contain data in the form of fields (attributes or properties) and code in the form of methods. OOP principles guide the design and implementation of software systems, promoting modularity, reusability, and maintainability.

In Java, "oops" typically stands for Object-Oriented Programming concepts. The pillars of Object-Oriented Programming (OOP) in Java are:

1. **Encapsulation**: Encapsulation is the bundling of data (variables) and methods (functions) that operate on the data into a single unit called a class. It helps in data hiding and protects the internal state of an object from external interference.

2. **Inheritance**: Inheritance is a mechanism where one class inherits properties and behavior from another class. The class that is inherited from is called the superclass or base class, and the class that inherits is called the subclass or derived class. Inheritance promotes code reusability and establishes a relationship between classes.

3. **Polymorphism**: Polymorphism allows objects to be treated as instances of their parent class. It enables methods to do different things based on the object that invokes them. There are two types of polymorphism in Java: compile-time polymorphism (method overloading) and runtime polymorphism (method overriding).

4. **Abstraction**: Abstraction is the process of hiding the implementation details and showing only the essential features of an object. It allows you to focus on what an object does rather than how it does it. Abstract classes and interfaces are used to achieve abstraction in Java.

These pillars form the foundation of object-oriented programming and are essential for creating modular, scalable, and maintainable Java applications.

----

### Encapsulation
**Definition**: Encapsulation is one of the core principles of OOP that involves bundling the data (attributes) and methods (functions) that operate on the data into a single unit called a class. It restricts direct access to some of the object's components, providing controlled access through methods.

#### Key Aspects of Encapsulation:
**Data Hiding**: Encapsulation hides the internal state (data) of an object, allowing access only through methods. This prevents direct modification of object attributes and ensures data integrity.

**Access Modifiers**: In Java, access modifiers such as private, public, protected, and default are used to control access to class members. Private members are accessible only within the class, while public members can be accessed from any other class.

**Getter/Setter Methods**: Encapsulation typically involves using getter methods (accessors) to retrieve private field values and setter methods (mutators) to set or update private field values. This controlled access enhances security and validation.

**Maintains Integrity**: By encapsulating data and providing controlled access, encapsulation protects the object's state from external interference, ensuring that it remains consistent and valid.

**Enhances Modularity**: Encapsulation promotes modularity by keeping related data and methods together within a class. This reduces coupling between classes and improves code organization and maintenance.

### 1. Encapsulation Example:

```java
// Encapsulation Example
public class Person {
    private String name;
    private int age;

    // Getter and setter methods for name
    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    // Getter and setter methods for age
    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        if (age >= 0) {
            this.age = age;
        } else {
            System.out.println("Age cannot be negative.");
        }
    }
}

public class Main {
    public static void main(String[] args) {
        // Creating a Person object
        Person person = new Person();
        
        // Using setter methods to set values
        person.setName("John Doe");
        person.setAge(30);

        // Using getter methods to retrieve values
        System.out.println("Name: " + person.getName());
        System.out.println("Age: " + person.getAge());
    }
}
```

**Explanation:**
- Encapsulation is demonstrated through the `Person` class where data (name and age) is encapsulated using private fields and accessed through getter and setter methods.
- Getter methods (`getName()`, `getAge()`) retrieve the values of private fields, while setter methods (`setName()`, `setAge()`) set or update the values while applying validation logic.
- This approach ensures controlled access to object properties and maintains data integrity.
---

### 3. Access Modifiers :

**Definition:** Access modifiers in Java control the visibility and accessibility of classes, methods, and variables within a program.

#### Key Aspects of Access Modifiers:

![image](https://github.com/Akmeena4u/JAVA-Complete-Course/assets/93425334/5a5b1256-d76c-4694-af98-41d31c3184c2)


1. **Types:** Java has four access modifiers: `public`, `protected`, default (no modifier), and `private`.

2. **Public:** The `public` modifier allows access from any other class, including classes from other packages.

3. **Protected:** The `protected` modifier allows access within the same package and by subclasses (inheritance).

4. **Default (No Modifier):** If no access modifier is specified, it's the default, allowing access only within the same package (package-private).

5. **Private:** The `private` modifier restricts access to the defining class only, making the member inaccessible from outside the class.

6. **Class-Level Access:** Top-level classes can have `public` or default (no modifier) access. Nested and inner classes can have additional access modifiers.

7. **Member-Level Access:** Methods, constructors, and variables can use all four access modifiers to control visibility and access rules.


```java
// Access Modifiers Example
package com.example;

public class Person {
    private String name;  // Private access modifier

    public String getName() {  // Public getter method
        return name;
    }

    public void setName(String name) {  // Public setter method
        this.name = name;
    }
}

public class Main {
    public static void main(String[] args) {
        Person person = new Person();
        person.setName("Alice");

        // Accessing private field indirectly using public getter method
        System.out.println("Name: " + person.getName());
    }
}
```

**Explanation:**
- The `Person` class has a private field `name`, which can be accessed only within the `Person` class.
- Public getter and setter methods (`getName()`, `setName()`) allow controlled access to the private field, maintaining encapsulation and data integrity.
- Indirect access to the private field is achieved through public methods, ensuring controlled modification of object properties.

---

### 8.5 Getter and Setter Methods

**Definition:** Getter and setter methods are used to retrieve and modify the private fields (attributes) of a class, respectively.

#### Key Points about Getter and Setter Methods:

1. **Getters:** Getter methods retrieve the values of private fields and are typically named using the pattern `get<FieldName>`.

2. **Setters:** Setter methods set or update the values of private fields and are usually named using the pattern `set<FieldName>`.

3. **Control and Validation:** Getter and setter methods offer controlled access to class fields, allowing for validation logic to be implemented within the methods.

4. **Encapsulation:** Getter and setter methods facilitate encapsulation by providing read-only or write-only access to class fields, maintaining data integrity and security.

5. **Flexibility:** Using getter and setter methods allows for internal changes to the implementation of class fields without affecting external interfaces, enhancing flexibility and maintainability.
   
#### 4. Getter and Setter Methods Example:

```java
// Getter and Setter Methods Example
public class Rectangle {
    private double length;
    private double width;

    public double getLength() {
        return length;
    }

    public void setLength(double length) {
        if (length > 0) {
            this.length = length;
        } else {
            System.out.println("Invalid length.");
        }
    }

    public double getWidth() {
        return width;
    }

    public void setWidth(double width) {
        if (width > 0) {
            this.width = width;
        } else {
            System.out.println("Invalid width.");
        }
    }

    public double calculateArea() {
        return length * width;
    }
}

public class Main {
    public static void main(String[] args) {
        Rectangle rectangle = new Rectangle();
        rectangle.setLength(5.0);
        rectangle.setWidth(3.0);

        System.out.println("Length: " + rectangle.getLength());
        System.out.println("Width: " + rectangle.getWidth());
        System.out.println("Area: " + rectangle.calculateArea());
    }
}
```

**Explanation:**
- The `Rectangle` class encapsulates properties (`length` and `width`) using private fields and provides getter and setter methods for controlled access.
- Getter methods (`getLength()`, `getWidth()`) retrieve the values of private fields, while setter methods (`setLength()`, `setWidth()`) set or update the values with validation logic.
- Encapsulation is maintained to ensure data integrity and provide a clean interface for interacting with object properties.
