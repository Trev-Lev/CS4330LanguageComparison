##### Singleton

A singleton is a class where only one instance of itself can exist at a time. They are designed by making the constructor to the class private, and by writing a static method that has the return type of the singleton class. Due to the constructor being private, the static method (named something like getInstance()) is called to retrieve the single instance of the class.

Lazy instantiation/initialization is referenced in this document - an easy way to think of it is not initializing variables until they are needed.

##### Java

In Java, the singleton is implemented just like mentioned above. It can be [lazily instantiated](https://en.wikipedia.org/wiki/Lazy_initialization) and can be made thread safe. Here are some ways to do this:
- At the time of class loading, create the singleton instance (this is **not** lazy instantiation)
- Synchronize the static method for retrieving the instance (synchronization guarantees thread safety)

##### Kotlin

In Kotlin, singletons are easier to implement than in Java. Rather than creating a class, we can use an object:

```Kotlin
    // This is literally it
    object Singleton {
        init {
            // optional initialization code if needed
        }
    }
```

While this looks incredibly simple, that isn't all. The singleton is lazily instantiated upon its first access AND thread-safe.

The code above is compiled into Java code with a constructor and a single instance allowed, and is only used for simple singleton objects.

[Back to main](../README.md)
