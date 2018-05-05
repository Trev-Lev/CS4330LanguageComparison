##### Listeners and event handlers

###### Java

In Java, the implementation of listeners and event handlers is typically done through interfaces. An example:

```Java
    // Add resizable listener
    //  newlines for formatting purposes
    ChangeListener<Number> lambdaChangeListener =
     (ObservableValue<? extends Number> observable,
      Number oldValue, final Number newValue) -> {
        refresh();
    };

    stage.widthProperty().addListener(lambdaChangeListener);
    stage.heightProperty().addListener(lambdaChangeListener);

```

Where ChangeListener is an interface accessible through importing javafx.beans.value.ChangeListener. The listener is a lambda expression in an object (though it is not necessary to use a lambda expression), and added to both the widthProperty and the heightProperty of the stage in a javafx program.

###### Kotlin

Kotlin improved upon the ability to add event handlers and listeners from Java with its ability to use lambda expressions and pass them as arguments. Even in the code below, there are many different ways to write it:
```Kotlin
    // Example by Daniele Bottillo

    // Declare lambda expression
    fun setOnClickListener(listener: (View) -> Unit)

    // Add the listener
    button.setOnClickListener({ view -> doSomething() })
```

And the above is perhaps the most 'convoluted' (in this case, hard to read) way to write it. It should be noted that it is still much easier on the eyes than the java example further above on the page.

[Back to main](../README.md)
