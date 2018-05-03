##### Comparisons of references and values

**The == or != operator:**

In Java, these operators compare references. They are used for checking to see if a reference is equal to null, comparing enum values, or if checking that two different references are in fact referencing the same object.

In Kotlin, these operators reference structural equality. According to Kotlinlang.org:
```Kotlin
    a == b
    // This becomes...
    a?.equals(b) ?: (b === null)
```

Meaning that this expression is actually equal to the .equals() method seen in Java.

**.equals()**

In Java, this compares two values for equality. This is what you want to use when you check if one string is equal to another.

**Referential Equality (Kotlin)**

Referential Equality (in Java, this is == or !=) is checked with the === or the !== operators in Kotlin. These check if two references are pointing to the same object.

[Back to main](../README.md)
