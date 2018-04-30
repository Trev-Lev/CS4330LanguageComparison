##### Classes

###### Java
Defining a class in Java is relatively simple.
```Java
class Bicycle {

    private String name;
    private int speed;

    // Empty constructor
    public Bicycle() {

    }

    // Constructor with two arguments
    public Bicycle(String name, int speed) {
        this.name = name;
        this.speed = speed;
    }

    // Implementation of Bicycle here
}
```

Classes that are implemented within another class can be labeled as private and accessed from only within the original class. In addition, a class stored in a separate document would need the public access modifier to be accessed from within another file.

Creating a new instance of a class is done with the keyword "new".
```Java
    // Create a new Bicycle object named bicycle
    Bicycle bicycle = new Bicycle();
```

The construction of the object "bicycle" above is done when the new keyword is used. The method known as the Constructor (the empty block of code shown above) is used to set fields when arguments are passed to the initial call.

```Java
    // Create a new Bicycle object with fields
    Bicycle bicycle = new Bicycle("Jimmy", 10);
```

In Java, destruction is not needed. When objects are no longer being used, a feature known as garbage collection will destroy the object and manage the memory for you.

###### Kotlin

Classes in Kotlin are defined in much the same way as they are in Java, via the class keyword, and if there is a class with no body then the brackets can be omitted:

```Kotlin
    class Bicycle {

    }

    class Empty
```

Kotlin does not have a "new" keyword. Objects are created by calling the constructor as if it were a function.

```Kotlin
    val bicycle = Bicycle("Jimmy")
```

Kotlin, like Java, does not have a native destructor as it runs on the JVM and has garbage collection.

[Back to main](../README.md)
