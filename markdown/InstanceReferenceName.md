##### Instance Reference Name

###### this
Java uses the keyword 'this' to refer to the current object. It is commonly used in constructors:

```Java
class Bicycle {

    private String name;

    public Bicycle (String name) {
        this.name = name;
    }
}
```

In the example above, the argument passed to the constructor has the same name as the field in the class. To properly set the field to the right value, the keyword 'this' is used to ensure that the field on the object itself is referenced.

Kotlin's 'this' denotes the current receiver. In a member of a class, it functions just as it would in Java - it refers to itself.
In an extension function or a function literal with a receiver, the keyword denotes the receiver that was passed (if none passed, it defers to the scope it is in).

Examples of Kotlin's non-Java like this, from Kotlin's website:
```Kotlin
    val funLit = lambda@ fun String.() {
        val d = this // funLit's receiver
    }

    class A {
        inner class B {
            fun Int.foo() {
                val a = this@A  // Refers to A
                val b = thisAB  // Refers to B
                val x = this    // Refers to foo()
            }
        }
    }
```

[Back to main](../README.md)
