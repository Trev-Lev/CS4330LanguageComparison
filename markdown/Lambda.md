##### Lambda expressions

###### Java

In Java 8, lambda expressions were introduced. They are viewed as Java's first step towards functional programming, and can be passed around as objects.

```Java
    StateOwner stateOwner = new StateOwner();

    stateOwner.addStateListener(
        (oldState, newState) -> System.out.println("State changed")
    );
```

Lambda expressions in Java work with **functional interfaces**, or interfaces with only one function. In the example above from http://tutorials.jenkov.com, the single function in the interface that StateOwner implements is compared to the parameters passed to it (in this case, oldState and newState). If the parameters match, the lambda expression is then turned into a function that implements the same interface as the parameter.

An example of a lambda expression as an object, from http://tutorials.jenkov.com:

```Java
    public interface MyComparator {
        public boolean compare(int a1, int a2);
    }

    MyComparator myComparator = (a1, a2) -> return a1 > a2;

    // Returns true if 2 > 5
    boolean result = myComparator.compare(2, 5);
```

###### Kotlin

Functions in Kotlin are specified as 'First-class', meaning that they can be stored in variables and data structures or passed/returned from higher order functions. A higher order function is a function that can return another function or take another function as a parameter.

However, Kotlin also has lambda expressions. The format of a lambda expression according to Kotlinlang.org is as follows:
```Kotlin
    val sum = { x: Int, y: Int -> x + y }
```

Where 'sum' is the object that holds the function, x and y are arguments passed to the function, and the function returns the sum of x and y. Unlike Java, a functional interface is not necessary to create a lambda expression.

[Back to main](../README.md)
