
###  Super Keyword:

The `super` keyword in Java is used to refer to the immediate superclass of the current object. It is primarily used to call superclass methods, access superclass variables, and invoke superclass constructors.

Uses of super Keywords in Java
• It is used to refer to an instance variable of the immediate parent class.
• It is used to invoke a method of the immediate parent class.
• It is used to invoke a constructor of immediate parent class.

```java
public class Animal {
    public void eat() {
        System.out.println("Animal is eating");
    }
}

public class Dog extends Animal {
    @Override
    public void eat() {
        super.eat();  // Calls the eat() method of the superclass
        System.out.println("Dog is eating");
    }
}
```

---
### Super v/s This 

Here's a tabular comparison between the `this` and `super` keywords in Java based on their usage:

| Feature                                     | `this` Keyword                                       | `super` Keyword                                             |
|---------------------------------------------|-------------------------------------------------------|--------------------------------------------------------------|
| Implicit Reference Variable                 | Represents the current class                          | Represents the immediate parent class                        |
| Invoking Methods                            | Invokes methods of the current class                  | Invokes methods of the immediate parent class                |
| Invoking Constructor                        | Invokes a constructor of the current class            | Invokes a constructor of the immediate parent class          |
| Refers to Variables                         | Refers to instance and static variables of the class  | Refers to instance and static variables of the parent class  |
| Usage in Return and Passing as an Argument  | Used to return and pass as an argument in the context of a current class object  | Used to return and pass as an argument in the context of an immediate parent class object  |

