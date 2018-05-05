##### Null/nil

Both Java and Kotlin use the term **null** to represent an empty object or null pointer.

Both Java and Kotlin also feature the NullPointerException for error handling regarding null, though one using Kotlin will find that a NullPointerException is thrown far less than in Java.

Kotlin offers more protection against errors than Java does, and its creators aimed to eliminate the danger that might occur from null references. Some ways Kotlin goes about doing this:

- Nullable variables: a variable defined as nullable (distinguished with a ? after its type) is allowed to hold null values. It is a compilation error if a non-nullable variable is set to null
- Along with nullable variables, collections can be nullable
- The safe call: "?" before a member of a variable is accessed to return the member if the variable is not null, and null otherwise.

[Back to main](../README.md)
