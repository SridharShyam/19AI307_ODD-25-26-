# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
```
The much-anticipated "Publishers Federation Book Expo" has returned, promising an even grander experience with nearly a million books on display. This year, the event is being hosted on the topmost floor—floor number N—of the prestigious Hotel Grand Regency.

Williams, a passionate book enthusiast, arrives at the expo and is now looking for the fastest way to reach the ground floor from the N-th floor. He has two options: take the stairs or use the elevator.

The stairs are built at a 45-degree angle, and Williams can descend them at a speed of V1 meters per second. Alternatively, the elevator always starts at the ground floor, travels up to the N-th floor to pick him up (the pickup is instantaneous), and then descends back to the ground floor at a speed of V2 meters per second.

The total vertical distance the elevator travels in one complete trip (up and down) is 2 × N meters. Meanwhile, the stairs span a diagonal length of √2 × N meters due to the 45-degree incline.

Your task is to help Williams choose the faster route. Based on the time it would take using either method, determine whether Stairs or Elevator is the better option.

Input :
N, V1, and V2 (Follow the same order).

Output :
Stairs if taking the stairs is faster, or Elevator if the elevator is the quicker option.
```

## AIM:
To write a Java program that uses a **conditional statement** to determine whether taking the **stairs or the elevator** is faster based on the given floor number and speeds.

## ALGORITHM :
1. Start the program.  
2. Import the necessary package `java.util`.  
3. Create a `Scanner` object to read the input values.  
4. Read the values of `N` (floor number), `V1` (speed of stairs), and `V2` (speed of elevator).  
5. Calculate the time taken using stairs using the formula:  
   `stairTime = (√2 × N) / V1`.  
6. Calculate the time taken using the elevator using the formula:  
   `elevatorTime = (2 × N) / V2`.  
7. Compare `stairTime` and `elevatorTime`.  
8. If `stairTime` is less than `elevatorTime`, print **"Stairs"**.  
9. Otherwise, print **"Elevator"**.  
10. End the program.

## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: SHYAM S
Register Number: 212223240156

import java.util.Scanner;

public class Main
{
    public static void main(String args[])
    {
        Scanner scan = new Scanner(System.in);
        int n=scan.nextInt();
        int v1=scan.nextInt();
        int v2=scan.nextInt();
        
        double stairTime=(Math.sqrt(2)*n)/v1;
        double elevatorTime=(2.0*n)/v2;
        
        if(stairTime < elevatorTime)
        {
            System.out.println("Stairs");
        }
        else
        {
            System.out.println("Elevator");
        }
    }
}
*/
```

## OUTPUT:

<img width="377" height="291" alt="image" src="https://github.com/user-attachments/assets/0a99dd0b-322c-4422-b7d2-4d6698ead252" />

## RESULT:
Thus, the Java program to determine the **faster route between stairs and elevator using conditional statements** was successfully executed and the output was verified.
