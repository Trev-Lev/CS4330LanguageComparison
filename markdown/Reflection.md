##### Reflection

Reflection is when methods, classes, and interfaces can be examined at runtime through code - the code that is written 'inspects' other code.

For Java, this is achieved through the reflection API: java.lang.reflect.

In Java, reflection can be used to invoke methods at runtime if its name and parameter types are known. Fields and methods can also be accessed without needing to use the proper access modifier to reach them. This can be useful for debugging purposes.

```Java
    // Get all of the methods of a class
    Method[] methods = cls.getMethods();
```

As Kotlin can be viewed as an improved version of Java, many of its reflection properties are the same, albeit with some few differences. For example, Kotlin can inspect both Java classes and Kotlin classes at runtime, with the .java property on the KClass object required to access a Java class. An example of the KClass object:

```Kotlin
    val c = MyClass::class
```

The reference above is of type KClass. This is the most basic reflection feature (according to Kotlinlang.org), and obtains the reference to a statically known Kotlin class.

[Back to main](../README.md)
