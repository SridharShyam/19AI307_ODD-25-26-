# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
```
At an international airport, only one Radar Control Tower exists. This tower is responsible for handling all flight communications regardless of how many flights are coming in. Each incoming flight must contact this tower to register its approach.

To ensure safety and consistency, all flights must communicate with the same instance of the tower. If multiple towers are created, it may lead to inconsistent instructions — a huge risk in aviation.

Your task is to simulate this system using the Singleton pattern.

Key Hint (Hidden in Story):
Only one control tower object should exist.

Every flight contacting it should register its name.

You should log the order of flights that contacted the tower.

Input Format:
First line: Integer n – number of incoming flights

Next n lines: Each line contains the flight name.

Output Format:
For each flight, print:

[FlightName] registered with Radar Control Tower. Total Flights: [count]


```

## AIM:
To develop a Java program that demonstrates the **Singleton design pattern (a SOLID principle concept)** by ensuring that only one instance of the `RadarControlTower` exists and is used by all incoming flights to register and maintain a consistent count.


## ALGORITHM :
1. Start the program.
2. Import the necessary package `java.util.Scanner` to read input from the user.
3. Create a class named `RadarControlTower`.
4. Declare a private static instance of the class.
5. Declare a private variable `flightCount` to keep track of registered flights.
6. Create a private constructor to prevent direct object creation.
7. Define a public static method `getInstance()` to return the single instance of the class.
8. Inside `getInstance()`, create the instance only if it does not already exist.
9. Create a method `registerFlight(String flight)` to increment and return the total number of flights.
10. Create a class `prog` containing the `main()` method.
11. Read the number of flights `n` using a `Scanner`.
12. Loop `n` times to read each flight name.
13. For each flight, call `getInstance()` to get the same `RadarControlTower` object.
14. Register the flight using `registerFlight()` and get the updated count.
15. Print the flight registration message along with the total count.
16. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: SHYAM S
RegisterNumber: 212223240156
*/

import java.util.*;

class RadarControlTower {
    //Type your code
    
    private static RadarControlTower instance;
    private int flightCount = 0;

    private RadarControlTower() {
    }

    public static RadarControlTower getInstance() {
        if (instance == null) {
            instance = new RadarControlTower();
        }
        return instance;
    }

    public int registerFlight(String flight) {
        flightCount++;
        return flightCount;
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();  // consume newline

        for (int i = 0; i < n; i++) {
            String flight = sc.nextLine();
            RadarControlTower tower = RadarControlTower.getInstance();
            int total = tower.registerFlight(flight);
            System.out.println(flight + " registered with Radar Control Tower. Total Flights: " + total);
        }
    }
}
```

## OUTPUT:

<img width="1217" height="207" alt="image" src="https://github.com/user-attachments/assets/4f0bebcf-91ea-4a3f-803a-72e46fe66e87" />

## RESULT:
Thus, the Java program demonstrating the **Singleton design pattern to ensure a single instance of Radar Control Tower for managing flight registrations** was successfully implemented and executed.
