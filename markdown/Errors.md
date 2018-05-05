##### Errors and exception handling

**Errors vs. Exceptions**

An exception is an unwanted or unexpected event that may occur during a program that can disrupt the flow of the program. They are "caught" to ensure that the program still runs smoothly. An Error is a more serious problem that may break the program, and the program should not be looking to catch errors.

###### Java

Error handling in Java is comprised of 5 words:
- try
- catch
- throw
- throws
- finally

To catch exceptions, the statements that may cause them must be placed in a try block, with a catch block of code following it for each exception.

```Java
    try {
        // the code that may cause an exception
        // typically an IDE will tell you
        //  if a statement might cause one
    }
    catch (ExceptionType1 exOb) {
        // exception handler for ExceptionType1
        //  the exception name is 'exOb'
    }
```

The exception handler will then handle the exception specified. In code like this, there can be one try statement, multiple catch statements, and one finally statement which will be executed every time.

The 'throw' and 'throws' statements are used elsewhere:
- 'throw' is used to explicitly throw an exception from anywhere
- 'throws' is used after the method signature but before the method body to indicate what exceptions might be thrown from it.

###### Kotlin

Like in Java, all exceptions in Kotlin are descendants of the class Throwable. An exception can be explicitly thrown with the 'throw' keyword, and try/catch statements operate very similar:

```Kotlin
    try {
        // some code
    }
    catch (e: SomeException) {
        // the exception block
    }
    finally {
        // the optional 'finally' block
    }
```

However, Kotlin exception handling is not identical to Java exception handling. For example, the try block may return a value, and the keyword 'Nothing' exists.

'Nothing' is used to denote code that can never be reached. In the example below, When the function is called, the compiler knows that the execution doesn't continue beyond the call:
```Kotlin
    fun fail(message: String): Nothing {
        throw IllegalArgumentException(message)
    }

    val s = person.name ?: fail("Name required")
    println(s)
```
The function never returns, as it is marked with 'Nothing'.

[Back to main](../README.md)
