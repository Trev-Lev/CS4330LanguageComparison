##### Memory Management

Java is well known for its memory management ability - the name of the language makes me think "Garbage Collection".

In both Java and Kotlin, all objects are placed onto "the heap". Whenever the heap is considered full, garbage collection runs and throws out whatever is considered garbage. The heap is divided into two spaces: the nursery and the old space.

The nursery is where 'younger' objects are kept, and when it becomes full, garbage collection runs. The garbage collector will 'promote' objects that have lived long enough to the old space, and destroy the objects that are no longer needed. It should be noted that the old space can also become full, in which case the garbage collector will act upon it and destroy objects that are no longer in use.

Automatic reference counting (ARC), found in Objective-c and Swift programming languages, is a way of counting behind the scenes the amount of references to each particular object. When the number hits 0, the object is marked for destruction and then removed from memory.

Java and Kotlin do NOT offer automatic reference counting due to there being little need for it with the garbage collection thread running in the background.

[Back to main](../README.md)
