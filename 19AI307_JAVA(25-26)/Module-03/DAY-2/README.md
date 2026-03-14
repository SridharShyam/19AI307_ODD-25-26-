# Ex.No:3(b) POLYMORPHISM

## QUESTION:
```
Write a Java program using method overloading to print student details. Create a class Student with:

print(String name)

print(String name, int age)

print(String name, int age, String dept)
```

## AIM:
To develop a Java program that demonstrates **polymorphism using method overloading** by printing student details with different sets of parameters such as **name**, **name and age**, and **name, age, and department**.

## ALGORITHM :
1. Start the program.
2. Import the necessary package `java.util.Scanner` to read input from the user.
3. Create a class named `Student`.
4. Define a method `print(String name)` to display only the student's name.
5. Define an overloaded method `print(String name, int age)` to display the student's name and age.
6. Define another overloaded method `print(String name, int age, String dept)` to display the student's name, age, and department.
7. Create a class `Main` containing the `main()` method.
8. Create a `Scanner` object to read input values from the user.
9. Read the required inputs such as names, ages, and department from the user.
10. Create an object of the `Student` class.
11. Call the overloaded `print()` methods with different parameters.
12. Display the student details accordingly.
13. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: SHYAM S
Register Number: 212223240156
*/

import java.util.Scanner;

class Student
{
    void print(String name)
    {
        System.out.println("Name: "+name);
    }
    void print(String name, int age)
    {
        System.out.println("Name: "+name+", Age: "+age);
    }
    void print(String name, int age, String dept)
    {
        System.out.println("Name: "+name+", Age: "+age+", Dept: "+dept);
    }
}

public class Main
{
    public static void main(String args[])
    {
        Scanner scan = new Scanner(System.in);
        
        String name1 = scan.nextLine();
        String name2 = scan.nextLine();
        int age = scan.nextInt();
        scan.nextLine();
        String name3 = scan.nextLine();
        int age2 = scan.nextInt();
        scan.nextLine();
        String dept = scan.nextLine();

        Student s = new Student();
        s.print(name1);
        s.print(name2, age);
        s.print(name3, age2, dept);
    }
}
```
## OUTPUT:



## RESULT:
Thus, the Java program demonstrating **polymorphism using method overloading in the Student class** was successfully implemented and executed.
