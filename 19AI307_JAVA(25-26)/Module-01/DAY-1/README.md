# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
```
Lovely is now a potion apprentice at the Wizardry Academy. Every potion has to be made by mixing ingredients of different data types like int, double, byte, and float.

However, the mixing cauldron accepts only one type at a time, so she has to type cast the ingredients to prepare the final mix.

Lovely experiments with explicit and implicit type casting to see how different types behave when converted into others.

Task:
Read four types of values:

An int

A double

A float

A byte

Perform the following conversions:

Convert the int to double (implicit)

Convert the double to int (explicit)

Convert the float to int (explicit)

Convert the byte to float (implicit)

Print the results of each conversion.

Input Format:
First line: Integer value

Second line: Double value

Third line: Float value

Fourth line: Byte value

Output Format:

Int to Double: <value>
Double to Int: <value>
Float to Int: <value>
Byte to Float: <value>
```
## AIM:
To write a Java program to perform implicit and explicit type casting between different data types such as int, double, float, and byte, and display the converted values.

## ALGORITHM :
1. Start the program.  
2. Import the `Scanner` class and create a scanner object to read input values.  
3. Read an `integer`, `double`, `float`, and `byte` value from the user.  
4. Perform **implicit type casting** from `int` to `double` and `byte` to `float`.  
5. Perform **explicit type casting** from `double` to `int` and `float` to `int`.  
6. Print the results of each conversion in the specified format.  
7. End the program.

## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: SHYAM S
Register Number: 212223240156

import java.util.Scanner;

public class Main
{
    public static void main(String args[])
    {
        Scanner scan = new Scanner(System.in);
        int i=scan.nextInt();
        double d=scan.nextDouble();
        float f=scan.nextFloat();
        byte b=scan.nextByte();
        
        double i_d = i;
        int d_i = (int) d;
        int f_i = (int) f;
        float b_f = b;
        System.out.println("Int to Double: "+i_d);
        System.out.println("Double to Int: "+d_i);
        System.out.println("Float to Int: "+f_i);
        System.out.println("Byte to Float: "+b_f);
    }
}
*/
```

## OUTPUT:

<img width="856" height="452" alt="image" src="https://github.com/user-attachments/assets/cecabab4-b992-41f5-bf96-7d7e3e8f2980" />

## RESULT:
Thus, the Java program to perform implicit and explicit type casting between different data types was successfully executed and the output was verified.
