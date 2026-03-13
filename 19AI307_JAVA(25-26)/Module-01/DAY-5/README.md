# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
```
Write a Java program to calculate the power of a given number.
```

## AIM:
To write a Java program that uses the **Math function** to calculate the **power of a given number**.

## ALGORITHM :
1. Start the program.  
2. Import the necessary package `java.util`.  
3. Create a `Scanner` object to read input values.  
4. Read the **base value** and **power value** from the user.  
5. Use the `Math.pow()` function to calculate the power of the given number.  
6. Store the result in a variable.  
7. Display the base, exponent, and the calculated result.  
8. End the program.

## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: SHYAM S
RegisterNumber: 212223240156
*/

import java.util.Scanner;

public class Main
{
    public static void main(String args[])
    {
        Scanner scan = new Scanner(System.in);
        double base=scan.nextDouble();
        double power=scan.nextDouble();
        double val=Math.pow(base,power);
        
        System.out.println(base+" raised to the power of "+power+" is: "+val);
    }
}
```

## OUTPUT:
<img width="941" height="320" alt="image" src="https://github.com/user-attachments/assets/6be09249-2bb3-4601-857c-a0d4a0cc79e4" />

## RESULT:
Thus, the Java program to **calculate the power of a given number using the Math.pow() function** was successfully executed and the output was verified.
