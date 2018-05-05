##### Multithreading

Multithreading is a feature of a language that allows for the concurrent execution of 2+ parts of a program in order to speed things up and maximize the CPU usage. It is called 'Multithreading' because each part of a program that does this is referred to as a thread, a lightweight process contained within a larger piece also called a process.

###### Java

In Java, threads can be created by either extending the Thread class or implementing the Runnable interface. In either situation, the method run() defines the actions that the thread takes once it has started via the start() method.

```Java
    // Example of a what a thread class may look like
    class Multithreading implements Runnable {
        public void run() {
            try {
                System.out.println("Thread " + Thread.currentThread().getId());
            } catch (Exception e) {
                // handle exception here
            }
        }
    }
```

In the above class, multiple copies of the class can be made and started in order to see different tasks be executed at the same time.

###### Kotlin

The same applies to Kotlin with implementing Runnable or extending Thread:

```Kotlin
    // Extending Thread
    class ExtendThread: Thread() {
        public override fun run() {
            println("${Thread.currentThread()}")
        }
    }
    // Implementing Runnable
    class ImplementRunnable: Runnable {
        public override fun run() {
            println("${Thread.currentThread()}")
        }
    }
```

Where the first block of code implements threading through extending Thread, and the second block of code does threading through implementing Runnable. Both threads will need to be started via the start() call in the main function.

In addition to this similarity with Java, Kotlin also offers coroutines. Coroutines are an alternate way to achieve concurrent execution. In Kotlin 1.1, they are still experimental, so threads may be more reliable at the moment. Due to their experimental status, I will not provide an example of them, but I will still describe them and how they are intended to function.

A coroutine is a computation that can be suspended without blocking a thread. This is good because blocking a thread is a relatively expensive task, and suspending a coroutine is very miniscule in comparison. However, coroutines can only be suspended at so called 'suspension points', a difference from its threading counterpart that can be stopped whenever. To block a coroutine, a call must be made to a suspend function, declared with the 'suspend' keyword placed before 'fun'.

[Back to main](../README.md)
