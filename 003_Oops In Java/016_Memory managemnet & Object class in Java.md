### 1. How Java Memory Works

Java memory management involves two primary memory areas: the **Heap Memory** and **Stack Memory**. Understanding how these work is crucial for optimizing performance and preventing memory-related issues.

#### Java Heap Memory

- **Usage**: Used by the Java Runtime Environment (JRE) to allocate memory to objects and JRE classes.
- **Creation**: Whenever an object is created, it is allocated in the heap space.
- **Accessibility**: Objects in the heap space have global access and can be referenced from anywhere in the application.
- **Garbage Collection**: The heap is managed by the garbage collector, which automatically deallocates memory for objects that are no longer referenced.

Example:
```java
public class Memory {
    public static void main(String[] args) { 
        int i = 1; // Line 2
        Object obj = new Object(); // Line 3
        Memory mem = new Memory(); // Line 4
        mem.foo(obj); // Line 5
    }
    
    private void foo(Object param) { // Line 6
        String str = param.toString(); // Line 7
        System.out.println(str); // Line 8
    }
}
```

In the above example:
- The integer `i` is stored in the stack.
- The `Object` instance `obj` is created in the heap.
- The `Memory` instance `mem` is also created in the heap.

#### Java Stack Memory

- **Usage**: Contains method-specific values that are short-lived and references to objects in the heap.
- **Method Invocation**: Whenever a method is invoked, a new block is created in the stack to hold local primitive values and references.
- **Lifecycle**: As soon as the method ends, the block becomes unused and available for the next method invocation.
- **Size**: Stack memory is typically smaller compared to heap memory.

Example (continued from above):
- When `foo` method is called, `param` (a reference to the `Object` instance) and `str` (a reference to a `String`) are stored in the stack.

### 2. Java Object Class

The `Object` class is the root of the class hierarchy in Java. Every class in Java implicitly extends the `Object` class, providing a set of methods that are inherited by all Java classes. This includes methods like `toString()`, `equals()`, `hashCode()`, `clone()`, `getClass()`, `notify()`, `notifyAll()`, and `wait()`.

#### Important Methods of Object Class

- **`getClass()`**: Returns the runtime class of the object.
- **`hashCode()`**: Returns a hash code value for the object.
- **`equals(Object obj)`**: Indicates whether some other object is "equal to" this one.
- **`toString()`**: Returns a string representation of the object.
- **`clone()`**: Creates and returns a copy of this object.
- **`notify()`**: Wakes up a single thread that is waiting on this object's monitor.
- **`notifyAll()`**: Wakes up all threads that are waiting on this object's monitor.
- **`wait()`**: Causes the current thread to wait until another thread invokes `notify()` or `notifyAll()` on this object.


#### 1. `getClass()`

This method returns the runtime class of the object. 

Example:
```java
public class Test {
    public static void main(String[] args) {
        Test obj = new Test();
        System.out.println("Class of obj: " + obj.getClass());
    }
}
```
Output:
```
Class of obj: class Test
```

#### 2. `hashCode()`

This method returns a hash code value for the object. It is used in hashing-based collections like `HashMap`, `HashSet`, etc.

Example:
```java
public class Test {
    public static void main(String[] args) {
        Test obj = new Test();
        System.out.println("Hash code of obj: " + obj.hashCode());
    }
}
```
Output:
```
Hash code of obj: [some integer value]
```

#### 3. `equals(Object obj)`

This method checks if some other object is "equal to" this one. The default implementation checks if the references are the same.

Example:
```java
public class Test {
    int data;

    public Test(int data) {
        this.data = data;
    }

    public static void main(String[] args) {
        Test obj1 = new Test(5);
        Test obj2 = new Test(5);
        System.out.println("obj1 equals obj2: " + obj1.equals(obj2));
    }
}
```
Output:
```
obj1 equals obj2: false
```

To compare the content, we need to override the `equals` method:
```java
@Override
public boolean equals(Object obj) {
    if (this == obj) return true;
    if (obj == null || getClass() != obj.getClass()) return false;
    Test test = (Test) obj;
    return data == test.data;
}
```
Output with overridden method:
```
obj1 equals obj2: true
```

#### 4. `toString()`

This method returns a string representation of the object.

Example:
```java
public class Test {
    int data;

    public Test(int data) {
        this.data = data;
    }

    @Override
    public String toString() {
        return "Test{data=" + data + "}";
    }

    public static void main(String[] args) {
        Test obj = new Test(5);
        System.out.println(obj.toString());
    }
}
```
Output:
```
Test{data=5}
```

#### 5. `clone()`

This method creates and returns a copy of the object. To use this method, the class must implement the `Cloneable` interface and override the `clone` method.

Example:
```java
public class Test implements Cloneable {
    int data;

    public Test(int data) {
        this.data = data;
    }

    @Override
    protected Object clone() throws CloneNotSupportedException {
        return super.clone();
    }

    public static void main(String[] args) {
        try {
            Test obj1 = new Test(5);
            Test obj2 = (Test) obj1.clone();
            System.out.println("obj1 data: " + obj1.data);
            System.out.println("obj2 data: " + obj2.data);
        } catch (CloneNotSupportedException e) {
            e.printStackTrace();
        }
    }
}
```
Output:
```
obj1 data: 5
obj2 data: 5
```

#### 6. `finalize()`

This method is called by the garbage collector before the object is destroyed. It is used to perform cleanup operations.

Example:
```java
public class Test {
    @Override
    protected void finalize() throws Throwable {
        System.out.println("Object is being garbage collected");
    }

    public static void main(String[] args) {
        Test obj = new Test();
        obj = null;
        System.gc();
    }
}
```
Output:
```
Object is being garbage collected
```

#### 7. `notify()`, `notifyAll()`, `wait()`

These methods are used for thread communication. They can only be called from synchronized methods or blocks.

Example:
```java
public class Test {
    private static final Object lock = new Object();

    public static void main(String[] args) {
        Thread t1 = new Thread(() -> {
            synchronized (lock) {
                try {
                    System.out.println("Thread 1 waiting");
                    lock.wait();
                    System.out.println("Thread 1 resumed");
                } catch (InterruptedException e) {
                    e.printStackTrace();
                }
            }
        });

        Thread t2 = new Thread(() -> {
            synchronized (lock) {
                System.out.println("Thread 2 notifying");
                lock.notify();
            }
        });

        t1.start();
        try {
            Thread.sleep(1000); // Ensures t1 starts and waits
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
        t2.start();
    }
}
```
Output:
```
Thread 1 waiting
Thread 2 notifying
Thread 1 resumed
```

### Summary

The `Object` class methods provide a foundation for all Java classes. Understanding and properly utilizing these methods can greatly enhance the functionality and efficiency of your Java programs.
