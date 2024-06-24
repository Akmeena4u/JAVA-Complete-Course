Constructor chaining in Java refers to the process of one constructor calling another constructor within the same class. This allows for code reusability and avoids duplicating initialization logic. Here's an explanation of constructor chaining with an example:

### How Constructor Chaining Works:

1. **Calling Another Constructor:**
   - Within a constructor, you can use the `this()` keyword followed by the appropriate arguments to call another constructor in the same class.
   - This must be the first statement in the constructor body.

2. **Passing Arguments:**
   - When calling another constructor using `this()`, you can pass arguments to specify which version of the constructor to invoke.
   - This allows for different initialization logic based on the arguments passed.

3. **Chain of Calls:**
   - Constructor chaining can create a chain of constructor calls, where one constructor calls another, and so on, until the chain is complete.

### Example of Constructor Chaining:

```java
public class Car {
    private String brand;
    private int year;

    // Parameterized Constructor 1
    public Car(String brand, int year) {
        this.brand = brand;
        this.year = year;
    }

    // Parameterized Constructor 2 - Constructor chaining
    public Car(String brand) {
        this(brand, 2022); // Calls Parameterized Constructor 1 with default year
    }

    // Default Constructor - Constructor chaining
    public Car() {
        this("Toyota"); // Calls Parameterized Constructor 2 with default brand and year
    }

    public void displayDetails() {
        System.out.println("Brand: " + brand);
        System.out.println("Year: " + year);
    }
}
```

In this example:

- The first constructor `public Car(String brand, int year)` is a parameterized constructor that initializes the brand and year of the car.
- The second constructor `public Car(String brand)` is also a parameterized constructor but calls the first constructor using `this(brand, 2022)` to set the default year.
- The third constructor `public Car()` is a default constructor but calls the second constructor using `this("Toyota")` to set the default brand and year.

### Benefits of Constructor Chaining:

1. **Code Reusability:**
   - Constructor chaining allows you to reuse initialization logic by calling other constructors with different arguments.

2. **Flexibility:**
   - It provides flexibility to create objects with different initialization configurations without duplicating code.

3. **Initialization Order:**
   - Constructor chaining ensures that the necessary initialization steps are performed in the correct order, maintaining object integrity.

In summary, constructor chaining in Java enables one constructor to call another constructor within the same class, facilitating code reusability, flexibility in initialization, and ensuring proper object initialization order.
