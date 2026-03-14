# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
```
Create a class Course with attributes code, title, credits.
```

## AIM:
To create a class named **Course** with attributes **code**, **title**, and **credits**, create objects of the class, assign values using user input, and display the course details using Java.

## ALGORITHM :
1. Start the program.
2. Import the required package `java.util.Scanner` to read input from the user.
3. Create a class named `Course`.
4. Declare the attributes `code`, `title`, and `credits` inside the `Course` class.
5. Create the `Main` class containing the `main()` method.
6. Create a `Scanner` object to read input from the user.
7. Create the first object `c1` of the `Course` class.
8. Read the course code, title, and credits from the user and store them in `c1`.
9. Create the second object `c2` of the `Course` class.
10. Read the course code, title, and credits from the user and store them in `c2`.
11. Display the details of both courses in the format:
    `code | title | credits`.
12. Close the Scanner object.
13. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: SHYAM S
Register Number: 212223240156
*/

import java.util.Scanner;

class Course
{
    String code;
    String title;
    int credits;
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Course c1 = new Course();
        c1.code = sc.next();
        c1.title = sc.next();
        c1.credits = sc.nextInt();

        Course c2 = new Course();
        c2.code = sc.next();
        c2.title = sc.next();
        c2.credits = sc.nextInt();

        System.out.println(c1.code + " | " + c1.title + " | " + c1.credits + " credits");
        System.out.println(c2.code + " | " + c2.title + " | " + c2.credits + " credits");

        sc.close();
    }
}

```
## OUTPUT:



## RESULT:
Thus, the Java program to create a **Course class with attributes code, title, and credits**, create objects, assign values using user input, and display the course details was successfully implemented and executed.
