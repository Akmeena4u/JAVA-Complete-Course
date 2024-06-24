## Inheritance 

Inheritance is a fundamental concept in object-oriented programming (OOP) that allows a new class (subclass or derived class) to inherit properties and behaviors (methods and fields) from an existing class (superclass or base class). This concept promotes code reuse, modularity, and hierarchical organization of classes. Let's explore all about inheritance in Java with explanations and examples:

![image](https://github.com/Akmeena4u/JAVA-Complete-Course/assets/93425334/57a23403-a50b-4c1a-b2fb-c05839d3b924)


### 1. Basic Inheritance Syntax:

In Java, the `extends` keyword is used to establish inheritance between classes. Here's the basic syntax:

```java
public class Superclass {
    // Superclass members
}

public class Subclass extends Superclass {
    // Subclass members
}
```

---

### 2. Types of Inheritance in Java:

![image](https://github.com/Akmeena4u/JAVA-Complete-Course/assets/93425334/4b8cfe81-40df-4a5d-9e09-f63a7d7f68d3)


#### a. Single Inheritance:
In single inheritance, a subclass inherits from only one superclass.

```java
public class Animal {
    // Animal class members
}

public class Dog extends Animal {
    // Dog class members
}
```

#### b. Multilevel Inheritance:
In multilevel inheritance, a subclass inherits from another subclass, creating a chain of inheritance.

```java
public class Animal {
    // Animal class members
}

public class Mammal extends Animal {
    // Mammal class members
}

public class Dog extends Mammal {
    // Dog class members
}
```

#### c. Hierarchical Inheritance:
In hierarchical inheritance, multiple subclasses inherit from the same superclass.

```java
public class Animal {
    // Animal class members
}

public class Dog extends Animal {
    // Dog class members
}

public class Cat extends Animal {
    // Cat class members
}
```

#### d. Multiple Inheritance (Not Supported in Java):
*Java does not support multiple inheritance directly (a class inheriting from multiple classes). However, it supports multiple interface inheritance.*

```java
// Not supported in Java (syntax example only)
public class Subclass extends Superclass1, Superclass2 {
    // Subclass members
}
```

---

### 3. Access Modifiers in Inheritance:

- **Public:** Inherited members with public access modifier are accessible in the subclass and externally.
- **Protected:** Inherited members with protected access modifier are accessible in the subclass and subclasses (even if they are in different packages).
- **Default (Package-Private):** Inherited members with default access modifier are accessible only within the same package.
- **Private:** Inherited members with private access modifier are not accessible in the subclass.

---

### 4. Method Overriding:

1. Method overriding allows a subclass to provide a specific implementation for a method that is already defined in its superclass. The method signature in the subclass must match the method signature in the superclass.
2. In simple words  if a subclass provides the specific implementation of the method that has been declared by one of its parent class, it is known as methodverriding.
3. Method overriding is also known as runtime polymorphism. Hence, we can achieve Polymorphism in Java with the help of inheritance.
4. Java allows you to use the `@Override` annotation when overriding methods. This annotation helps in ensuring that the method is actually overriding a superclass method, providing compile-time checks.

```java
public class Animal {
    public void sound() {
        System.out.println("Animal makes a sound");
    }
}

public class Dog extends Animal {
    @Override
    public void sound() {
        System.out.println("Dog barks");
    }
}
```

---

### Conclusion:

Inheritance is a powerful mechanism in Java that promotes code reusability, modularity, and hierarchy in class structures. Understanding inheritance and its
