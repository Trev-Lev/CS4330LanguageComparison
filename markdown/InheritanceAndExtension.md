##### Inheritance by Extension

###### Java

In Java, classes can be extended to gain access to more methods (or fields, if they are not private)

```Java
    class Child extends Person {
        // Child can now access Person's methods
    }
```

In the above example, the class Child can now use members of the class Person. To call upon members explicitly, the keyword super is used.

You can use the extends keyword in an interface only if you are extending another interface. The methods in the extended interface will still have to be implemented somewhere down the line (likely the class that implements the interface that extends the other interfaces).

Overriding an inherited method in Java is done through the annotation @Override:

```Java
    @Override
    public void thisIsNew() {
        // new code
    }
```
###### Kotlin

Extension in Kotlin is different. All classes automatically implicitly inherit from the class 'Any':
```Kotlin
    class Example // Inherits from Any
```

By default, all classes in Kotlin are final (final has the same meaning here as it does in Java - it cannot be extended).
To make a class open for extension, it should be declared with the keyword open:

```Kotlin
    open class Example(p: Int) // empty
    class Derived(p: Int) : Example(p) // derived
```

The super keyword is also used in Kotlin by non-primary constructors to create the base type of the class.

Overriding in Kotlin is done with the override keyword, providing that the function being overridden is available to be overridden:

```Kotlin
    override fun thisIsNew(){
        // fun thisIsNew must be declared as 'open'
    }
```

[Back to main](../README.md)
