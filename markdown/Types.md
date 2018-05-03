##### Types

###### Java
Java supports 8 primitive data types:
- byte
- short
- int
- long
- float
- double
- boolean
- char

In addition to the 8 primitive types, a java.lang.String (a string) represents a string of characters. Arrays in Java are also of a fixed length.

###### Kotlin
Kotlin is a bit different than Java in that all types are objects. Here are some types:
- Long
- Int
- Short
- Byte
- Double
- Float
- Boolean
- Char

It should be noted that to declare an object or a variable, the val and the var keywords are used.
- val = constant
- var = mutable
Like Java, arrays cannot change size once they have been created.

##### Value / Reference Types
Java supports both value and reference types. Primitive types are passed and returned by value, and everything else is done by reference. Java is viewed as a pass-by-value language, but it largely depends on what is meant by reference. In Java, a declaration of a variable is actually a pointer to that variable, and likewise a pointer to a variable is what is returned at the end of a non-void (and non boolean) function - and that pointer never changes.

Kotlin runs on the same JVM and functions the same as above, albeit with a different appearance.

##### Can new value types be created?
In neither Java nor Kotlin can new primitive/basic types be created, so the answer to the question "Can new value types be created?" is no.

Both languages support the creation of new objects (Java in classes, Kotlin in classes and data classes), but these are passed by value (a pointer) in the same manner as mentioned earlier in the document.

[Back to main](../README.md)
