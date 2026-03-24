# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
```
Read a file and print only the lines containing the word "Java".
```

## AIM:
To develop a Java program that demonstrates **file handling** by reading data from a file and printing only the lines that contain the word **"Java"**.

## ALGORITHM :
1. Start the program.
2. Import the necessary packages `java.io.*` and `java.util.*`.
3. Create a class named `Main`.
4. Inside the `main()` method, create a `Scanner` object to read input from the user.
5. Create a `FileWriter` object to write user input into a file (`data.txt`).
6. Continuously read lines from the user until the user enters `"exit"`.
7. Write each input line into the file.
8. Close the `FileWriter` to save the data.
9. Create a `BufferedReader` object to read data from the file.
10. Read each line from the file one by one.
11. Check if the line contains the word `"Java"`.
12. If it contains the word, print the line.
13. Continue until all lines are read.
14. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: SHYAM S
RegisterNumber: 212223240156
*/

import java.io.*;
import java.util.*;

public class Main
{
    public static void main(String args[]) throws IOException
    {
        Scanner scan = new Scanner(System.in);
        FileWriter wr = new FileWriter("data.txt");
        while(true)
        {
            String line = scan.nextLine();
            if(line.equals("exit")) break;
            wr.write(line+"\n");
        }
        wr.close();
        BufferedReader br = new BufferedReader(new FileReader("data.txt"));
        String line;
        System.out.println("Lines containing the word 'Java':");
        while((line=br.readLine())!=null)
        {
            if(line.contains("Java"))
            {
                System.out.println(line);
            }
        }
    }
}
```
## OUTPUT:

<img width="1012" height="312" alt="image" src="https://github.com/user-attachments/assets/ed979ba4-eea5-4d02-be71-2ea495d2e265" />

## RESULT:
Thus, the Java program demonstrating **file handling by reading a file and printing only the lines containing the word "Java"** was successfully implemented and executed.
