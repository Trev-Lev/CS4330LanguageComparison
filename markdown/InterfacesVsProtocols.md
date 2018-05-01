##### Interfaces vs Protocols

###### Java

Java supports interfaces. Interfaces in Java function to ensure that a class implementing them must define the methods in the interface. In Java, they are similar to abstract classes, with the main difference being that no method body can be declared in an interface - they must be defined separately in every class that implements that particular interface.

 An example:
```Java
    public interface Edible {
        public void consume();
    }

    public class Apple implements Edible {

        public void consume() {
            // Implementation here...
        }
    }
```

The class that implements the interface in Java **must** define the method body for the methods defined in the interface.

###### Kotlin

Interfaces in Kotlin are very similar to interfaces in Java. For example, the interface Edible from before:
```Kotlin
    interface Edible {
        fun consume() {
          // optional body
        }
    }
```
A primary difference (one that can be seen above) is that interfaces in Kotlin can be treated as abstract classes in Java, with the difference being that interfaces cannot hold state.

```Kotlin
    class Child : Edible {
        override fun consume() {
            println("Mmm, tasty!")
        }
    }
```

Both Java and Kotlin can implement multiple interfaces.

[Back to main](../README.md)
