# Ex.No:3(E) INNER CLASS

## QUESTION:
```
 Write a Java program where the inner class is declared private and accessed through a method in the outer class. 
```

## AIM:
To develop a Java program that demonstrates the use of a **private inner class** and shows how it can be accessed through a method of the outer class.


## ALGORITHM :
1. Start the program.
2. Import the necessary package `java.util.Scanner` to read input from the user.
3. Create an outer class named `Outer`.
4. Declare a **private inner class** named `Inner` inside the `Outer` class.
5. Define a method `display(int n)` inside the `Inner` class to print the given value.
6. Create a method `accessInner(int n)` in the `Outer` class.
7. Inside this method, create an object of the private inner class `Inner`.
8. Call the `display()` method using the inner class object.
9. Create a class `Main` containing the `main()` method.
10. Create a `Scanner` object to read input from the user.
11. Read an integer value from the user.
12. Create an object of the `Outer` class.
13. Call the `accessInner()` method and pass the input value.
14. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: SHYAM S
Register Number: 212223240156
*/

import java.util.*;

class Outer {

    private class Inner {
        void display(int n) {
            System.out.println("Data set inside private inner class: " + n);
        }
    }

    void accessInner(int n) {
        Inner obj = new Inner();
        obj.display(n);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();

        Outer o = new Outer();
        o.accessInner(n);
    }
}
```

## OUTPUT:



## RESULT:
Thus, the Java program demonstrating the use of a **private inner class accessed through a method of the outer class** was successfully implemented and executed.
