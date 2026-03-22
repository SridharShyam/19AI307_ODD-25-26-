# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
You wrote a program that stores some input strings into a String array and prints each string in uppercase.
However, you're getting a NullPointerException.
What should you check in your array before calling .toUpperCase() on a element?

## AIM:
To develop a Java program that demonstrates **exception handling** by identifying and handling a **NullPointerException**, ensuring that a string is not null before calling the `toUpperCase()` method.

## ALGORITHM :
1. Start the program.
2. Import the necessary package `java.util.Scanner` to read input from the user.
3. Create a class named `Main`.
4. Inside the `main()` method, create a `Scanner` object.
5. Read a string input from the user.
6. Use a `try` block to handle potential exceptions.
7. Check whether the input string is equal to `"null"`.
8. If it is `"null"`, manually throw a `NullPointerException`.
9. Otherwise, convert the string to uppercase using `toUpperCase()` and display it.
10. Use a `catch` block to handle the `NullPointerException`.
11. Display an appropriate message such as `"Null element"` when the exception occurs.
12. Stop the program.
13. 
## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: SHYAM S
RegisterNumber: 212223240156
*/

import java.util.Scanner;

public class Main
{
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        String str = sc.nextLine();

        try
        {
            if(str.equals("null"))
            {
                throw new NullPointerException();
            }

            System.out.println(str.toUpperCase());
        }
        catch(NullPointerException e)
        {
            System.out.println("Null element");
        }
    }
}
```
## OUTPUT:

<img width="561" height="262" alt="image" src="https://github.com/user-attachments/assets/cb830bdc-ba58-4fa2-a3f0-6a9b77d29748" />

## RESULT:
Thus, the Java program demonstrating **exception handling for NullPointerException by checking for null values before calling methods** was successfully implemented and executed.
