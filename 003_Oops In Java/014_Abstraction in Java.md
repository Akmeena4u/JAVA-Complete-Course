### What is Abstraction
The abstract class in Java cannot be instantiated (we cannot create objects of abstract classes). We use the abstract keyword to declare an abstract class.
• An abstract class can have both the regular methods and abstract methods.
• A method that doesn't have its body is known as an abstract method.
• Though abstract classes cannot be instantiated, we can create subclasses\from it. We can then access members of the abstract class using the object of the subclass.
• If the abstract class includes any abstract method, then all the child classes inherited from the abstract superclass must provide the implementation of the abstract method.

#### Core Principle of Abstraction:
- **Hides Complex Implementation**: Abstraction focuses on concealing intricate implementation details, showcasing only essential features to users.
- **Functionality Focus**: It emphasizes what an object does rather than how it accomplishes it, achieved through clear and well-defined interfaces.

#### Key Benefits of Abstraction:
- **Simplifies Complexity**: By presenting only relevant information in class design, abstraction reduces complexity, making code more manageable and understandable.
- **Real-World Modelling**: Abstraction enables the creation of objects that mimic real-life entities, capturing their essential attributes and behaviors effectively.

---

### Abstract Keyword

![image](https://github.com/Akmeena4u/JAVA-Complete-Course/assets/93425334/e3df4450-4119-4b4b-be97-74627151881f)


#### Abstract Class:
- **Non-instantiable Base Class**: Abstract classes are declared using the `abstract` keyword and cannot be instantiated on their own, serving as base classes for other classes.
- **Defining Abstract Methods**: Abstract classes can include abstract methods, which are methods without implementations, leaving specific functionality to be implemented by subclasses.
-```
 abstract class Shape {
    abstract void draw(); // Abstract method
    void display() {
        System.out.println("Displaying shape."); // Concrete method
    }
}```


#### Abstract Method:
- **Method without Implementation**: Abstract methods are defined in abstract classes but lack implementation details, allowing subclasses to provide their specific functionality.
- **Mandatory Implementation**: Subclasses inheriting from an abstract class must implement all abstract methods, ensuring complete functionality.

#### Design Flexibility:
- **Flexible Class Design**: Abstract classes and methods provide a contract or blueprint for subclasses to follow, offering design flexibility while enforcing specific behaviors.
- **Defining a Contract**: Abstract classes define a contract or set of rules that subclasses must adhere to, promoting consistency and structure in the codebase.

Abstraction plays a crucial role in software design by simplifying complexity, promoting modularity, and facilitating real-world modeling, ultimately leading to more maintainable and extensible codebases.
