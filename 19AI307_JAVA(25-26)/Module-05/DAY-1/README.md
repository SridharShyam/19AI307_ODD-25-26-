# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
```
Write a program to read user input from the keyboard using InputStreamReader
```

## AIM:
To develop a Java program that demonstrates reading user input from the keyboard using **InputStreamReader** along with **BufferedReader**.

## ALGORITHM :
1. Start the program.
2. Import the necessary package `java.io.*` to use input-output classes.
3. Create a class named `Main`.
4. Inside the `main()` method, create an `InputStreamReader` object to read input from the keyboard.
5. Wrap the `InputStreamReader` with a `BufferedReader` for efficient reading of input.
6. Use the `readLine()` method to read a line of text from the user.
7. Store the input in a string variable.
8. Display the input with a greeting message.
9. Handle possible exceptions using `throws IOException`.
10. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: SHYAM S
RegisterNumber: 212223240156
*/

import java.io.*;

public class Main
{
    public static void main(String args[]) throws IOException
    {
        InputStreamReader isr = new InputStreamReader(System.in);
        BufferedReader br = new BufferedReader(isr);
        
        String name = br.readLine();
        System.out.println("Hello, "+name+"!");
    }
}
```

## OUTPUT:

<img width="460" height="207" alt="image" src="https://github.com/user-attachments/assets/3e613aff-e560-43d0-a764-3d5628130789" />

## RESULT:

Thus, the Java program demonstrating reading user input using **InputStreamReader and BufferedReader** was successfully implemented and executed.
