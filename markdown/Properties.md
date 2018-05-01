##### Properties

###### Getters/Setters

In Java, getters and setters must be added for proper encapsulation to be achieved. Here is an example:

```Java
    class Bicycle {
        private String name;
        public Bicycle(){} // empty constructor

        public String getName() {
            return this.name;
        }

        public void setName(String name) {
            this.name = name;
        }
    }
```
The methods to get and set the field we wish to modify must be accessible from outside of the class, so they are public.

In Kotlin, getters and setters are created by default, with the exception being for constants (declared with keyword val) because a constant cannot be modified or set.

Moreover, the default getters and setters can be modified when the field is declared (examples from Kotlin website):

``` Kotlin
    var initialized = 1 // default getter and setter implied

    val isEmpty: Boolean
        get() = this.size == 0
```

###### Backing fields
A backing field is a private field on an object that stores data that can be manipulated through public methods.

In Java, this concept can lead to some error:
```Java
    // Credit to user glee8e on StackOverflow for the example
    // This is what Kotlin compiled to Java might do
    //  if programmed like a below example
    class Sample {
        private int counter = 0;
        // Infinite loop occurs here
        public void setCounter(int value) {
            if (value >= 0) setCounter(value);
        }
        public int getCounter() {
            return counter;
        }
    }
```
Where an infinite loop occurs when the setter calls itself.

Similarly in Kotlin:
``` Kotlin
    var i=0
    set(value){
        i = value
    }
```

Kotlin fixes this problem by not supporting fields, but properties. The field keyword can be used as a way to support backing variables.

The correct implementation of backing variables in Kotlin:
``` Kotlin
    // Credit to Eugen Pechanec on StackOverflow for the example
    class SomeClass {
    var counter: Int = 0
        set(value) {
            if (value >= 0) field = value   // field keyword
        }
    }
```

And changing to a version of Java that works:
``` Java
class Sample {
    private int counter = 0;
    // Infinite loop occurs here
    public void setCounter(int value) {
        if (value >= 0) this.counter = value;;
    }
    public int getCounter() {
        return counter;
    }
}
```

###### Computed Properties
Computed properties calculate a value rather than store one.
Technically, a computed property is a custom getter method, so in a sense they are supported in Java:

```Java
class Person {
    private int age;

    public int getAge() { return this.age;}
    public int getAgeInDogYears() { return this.age * 7;}
    //...
}
```
And in Kotlin:

``` Kotlin
// Credit to mfulton26 for the example on StackOverflow
class Banana {
    var ripeness = 1

    val color: String
        get() = when {
            ripeness > 80 -> "brown"
            ripeness > 50 -> "yellow"
            else -> "green"
        }
}
```
[Back to main](../README.md)
