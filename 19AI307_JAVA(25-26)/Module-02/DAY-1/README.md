# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
```
Create a class Course with attributes code, title, credits.
```

## AIM:


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	





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
