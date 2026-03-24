# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
```
Print "Hello" and "World" alternately from two threads using synchronized blocks.
```

## AIM:
To develop a Java program that demonstrates **multithreading with synchronization** by printing `"Hello"` and `"World"` alternately using two threads.


## ALGORITHM :
1. Start the program.
2. Import the necessary package `java.util.Scanner` to read input from the user.
3. Create a class `PrintTask` to handle synchronized printing.
4. Declare a boolean variable `helloTurn` to control the execution order of threads.
5. Create a synchronized method `printHello()`:
   - Use a `while` loop to wait if it is not the turn to print `"Hello"`.
   - Print `"Hello"`.
   - Change the turn to `"World"`.
   - Notify the waiting thread.
6. Create another synchronized method `printWorld()`:
   - Use a `while` loop to wait if it is not the turn to print `"World"`.
   - Print `"World"`.
   - Change the turn to `"Hello"`.
   - Notify the waiting thread.
7. Create a class `Main` containing the `main()` method.
8. Create a `Scanner` object to read the number of times `n`.
9. Create an object of `PrintTask`.
10. Create the first thread to call `printHello()` `n` times.
11. Create the second thread to call `printWorld()` `n` times.
12. Start both threads.
13. The threads execute alternately using synchronization.
14. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: SHYAM S
RegisterNumber: 212223240156
*/

import java.util.*;

class PrintTask {
    private boolean helloTurn = true;

    public synchronized void printHello() throws InterruptedException {
        while (!helloTurn) wait();

        System.out.println("Hello");
        helloTurn = false;
        notify();
    }

    public synchronized void printWorld() throws InterruptedException {
        while (helloTurn) wait();

        System.out.println("World");
        helloTurn = true;
        notify();
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        PrintTask task = new PrintTask();

        new Thread(() -> {
            try {
                for (int i = 0; i < n; i++)
                    task.printHello();
            } catch (Exception e) {}
        }).start();

        new Thread(() -> {
            try {
                for (int i = 0; i < n; i++)
                    task.printWorld();
            } catch (Exception e) {}
        }).start();
    }
}
```

## OUTPUT:

<img width="372" height="707" alt="image" src="https://github.com/user-attachments/assets/c3d7f206-cc63-49c6-8a0d-655954d63a28" />

## RESULT:
Thus, the Java program demonstrating **multithreading with synchronization to alternately print "Hello" and "World" using two threads** was successfully implemented and executed.
