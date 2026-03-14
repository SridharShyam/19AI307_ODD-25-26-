# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
```
Write a Java program to create a class called Rectangle with private instance variables length and width. Provide public getter and setter methods to access and modify these variables

import java.util.Scanner;

 class Rectangle {
    // Private instance variables
    private double length;
    private double width;

    // Getter and Setter for length
    public double getLength() {
        return length;
    }
    public void setLength(double length) {
        this.length = length;
    }

    // Getter and Setter for width
    public double getWidth() {
        return width;
    }
    public void setWidth(double width) {
        this.width = width;
    }

    // Method to calculate area
    public double calculateArea() {
        return length * width;
    }
}
```
## AIM:
To write a Java program that demonstrates the use of **access specifiers** by creating a `Rectangle` class with **private instance variables** `length` and `width`, and accessing them using **public getter and setter methods**.

## ALGORITHM :
1. Start the program.
2. Import the necessary package `java.util.Scanner` to read input from the user.
3. Create a class named `Rectangle`.
4. Declare two private instance variables `length` and `width`.
5. Create public getter methods `getLength()` and `getWidth()` to access the values of the private variables.
6. Create public setter methods `setLength()` and `setWidth()` to modify the values of the private variables.
7. Define a method `calculateArea()` to compute the area of the rectangle using `length × width`.
8. Create the `Main` class containing the `main()` method.
9. Create a `Scanner` object to read the length and width from the user.
10. Create an object of the `Rectangle` class.
11. Use the setter methods to assign the input values to the rectangle object.
12. Use the getter methods to retrieve and display the length and width.
13. Stop the program.
14. 
## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: SHYAM S
Register Number: 212223240156
*/

import java.util.Scanner;

class Rectangle {
    private double length;
    private double width;
    public double getLength() {
        return length;
    }
    public void setLength(double length) {
        this.length = length;
    }
    public double getWidth() {
        return width;
    }
    public void setWidth(double width) {
         this.width = width;
    }
    public double calculateArea() {
        return length * width;
    }
}
public class Main
{
    public static void main(String args[])
    {
        Scanner scan = new Scanner(System.in);
        Rectangle rect = new Rectangle();
        
        double length = scan.nextDouble();
        double width = scan.nextDouble();
        rect.setLength(length);
        rect.setWidth(width);
        
        System.out.println("Length: "+rect.getLength());
        System.out.println("Width: "+rect.getWidth());
    }
}
```
## OUTPUT:



## RESULT:
Thus, the Java program to demonstrate **access specifiers using private variables with public getter and setter methods in a Rectangle class** was successfully implemented and executed.
