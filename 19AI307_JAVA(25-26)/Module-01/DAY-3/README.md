# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
```
The factors of a number are all integers that divide the number exactly without leaving a remainder. For example:

Factors of 12 are 1, 2, 3, 4, 6, 12

Factors of 15 are 1, 3, 5, 15

Write a Java program that:

Prompts the user to enter a positive integer.

Finds and displays all the factors of the given number.

Uses a for loop to check each number from 1 to the given number to see if it divides the number
```

## AIM:
To write a Java program that uses a **looping statement (for loop)** to find and display all the **factors of a given positive integer**.

## ALGORITHM :
1. Start the program.  
2. Import the necessary package `java.util`.  
3. Create a `Scanner` object to read the input value.  
4. Read a positive integer `num` from the user.  
5. Display the message **"Factors:"**.  
6. Use a `for` loop to iterate from `1` to `num`.  
7. In each iteration, check if `num % i == 0`.  
8. If the condition is true, print the value of `i` as a factor.  
9. Repeat the process until the loop completes.  
10. End the program.

## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: SHYAM S
RegisterNumber: 212223240156
*/

import java.util.Scanner;

public class Main
{
    public static void main(String args[])
    {
        Scanner scan = new Scanner(System.in);
        
        int num=scan.nextInt();
        System.out.print("Factors:");
        
        for(int i=1;i<=num;i++)
        {
            if(num%i==0)
            {
                System.out.print(" "+i);
            }
        }
    }
}
```

## OUTPUT:
<img width="612" height="335" alt="image" src="https://github.com/user-attachments/assets/2147d7dc-1a65-423a-9357-7bc957033579" />

## RESULT:
Thus, the Java program to **find and display all the factors of a given number using a looping statement** was successfully executed and the output was verified.
