# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
```
Write a java program for set the priority and name of the current thread.Consider two threads t1 and t2

Note : Read the threadname from the User

set the priority as 4 for t1 and set the priority as 2 for t2
```

## AIM:
To develop a Java program that demonstrates **thread priority** by creating two threads, assigning them user-defined names, and setting their priorities.

## ALGORITHM :
1. Start the program.
2. Import the necessary package `java.util.Scanner` to read input from the user.
3. Create a class named `Main`.
4. Inside the `main()` method, create a `Scanner` object.
5. Read two thread names from the user.
6. Create two thread objects `t1` and `t2`.
7. Set the names of the threads using `setName()`.
8. Set the priority of thread `t1` as `4`.
9. Set the priority of thread `t2` as `2`.
10. Display the thread details using `System.out.println()`.
11. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: SHYAM S
RegisterNumber: 212223240156
*/

import java.util.*;

public class Main
{
    public static void main(String args[])
    {
        Scanner scan = new Scanner(System.in);
        String name1=scan.nextLine();
        String name2=scan.nextLine();
        
        Thread t1=new Thread();
        Thread t2=new Thread();
        
        t1.setName(name1);
        t2.setName(name2);
        t1.setPriority(4);
        t2.setPriority(2);
        
        System.out.println(t1);
        System.out.println(t2);
    }
}
```

## OUTPUT:

<img width="787" height="248" alt="image" src="https://github.com/user-attachments/assets/6222efe6-ebd3-4177-a4e8-f1c30c685ddd" />

## RESULT:
Thus, the Java program demonstrating **setting thread names and priorities for multiple threads** was successfully implemented and executed.
