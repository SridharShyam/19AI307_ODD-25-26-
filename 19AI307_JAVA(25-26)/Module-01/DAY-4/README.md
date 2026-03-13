# Ex.No:1(D) ARRAYS

## QUESTION:
```
Write a Java program to count how many elements in an array are divisible by 3 or 5
```

## AIM:
To write a Java program that uses the **array concept** to count the number of elements in an array that are **divisible by 3 or 5**.

## ALGORITHM :
1. Start the program.  
2. Import the necessary package `java.util`.  
3. Create a `Scanner` object to read input values.  
4. Read the number of elements `n` from the user.  
5. Declare an array of size `n`.  
6. Initialize a variable `count` to 0.  
7. Use a `for` loop to read `n` elements into the array.  
8. For each element, check if it is divisible by `3` or `5` using the condition `(arr[i] % 3 == 0 || arr[i] % 5 == 0)`.  
9. If the condition is true, increment the `count`.  
10. After the loop ends, display the value of `count`.  
11. End the program.

## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: SHYAM S
RegisterNumber: 212223240156
*/

import java.util.Scanner;

public class Main
{
    public static void main(String args[])
    {
        Scanner scan = new Scanner(System.in);
        int n=scan.nextInt();
        int[] arr = new int[n];
        int count=0;
        
        for(int i=0;i<n;i++)
        {
            arr[i]=scan.nextInt();
            if(arr[i]%3==0 || arr[i]%5==0)
            {
                count++;
            }
        }
        System.out.println(count);
    }
}
```

## OUTPUT:

<img width="333" height="596" alt="image" src="https://github.com/user-attachments/assets/b3232d10-9d1c-4cd4-bcc5-fdd66addd675" />

## RESULT:
Thus, the Java program to **count the number of elements in an array that are divisible by 3 or 5** was successfully executed and the output was verified.
