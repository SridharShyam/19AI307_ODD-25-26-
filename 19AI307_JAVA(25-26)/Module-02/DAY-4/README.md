# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
```
Implement a class Employee with a parameterized constructor to initialize id, name, and salary.
```

## AIM:
To develop a Java program that demonstrates **variable scope and the use of a parameterized constructor** by creating an `Employee` class to initialize and display the employee details such as **id, name, and salary**.

## ALGORITHM :
1. Start the program.
2. Import the necessary package `java.util.Scanner` to read input from the user.
3. Create a class named `Employee`.
4. Declare private instance variables `id`, `name`, and `salary`.
5. Create a **parameterized constructor** that receives `id`, `name`, and `salary` as parameters and initializes the instance variables using `this` keyword.
6. Define a method `display()` to print the employee details.
7. Create a class `Main` containing the `main()` method.
8. Create a `Scanner` object to read input values from the user.
9. Read employee id, name, and salary from the user.
10. Create an object of the `Employee` class by passing the input values to the constructor.
11. Call the `display()` method to print the employee details.
12. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: SHYAM S
Register Number: 212223240156
*/

import java.util.Scanner;

class Employee {
    private int id;
    private String name;
    private double salary;
    public Employee(int id, String name, double salary) {
        this.id = id;
        this.name = name;
        this.salary = salary;
    }
    public void display() {
        System.out.println("Employee Details:");
        System.out.println("Employee ID: " + id);
        System.out.println("Employee Name: " + name);
        System.out.println("Employee Salary: " + salary);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);

        int id = scan.nextInt();
        scan.nextLine();
        String name = scan.nextLine();
        double salary = scan.nextDouble();
        Employee emp = new Employee(id, name, salary);
        emp.display();
    }
}
```
## OUTPUT:



## RESULT:
Thus, the Java program to demonstrate **variable scope and the use of a parameterized constructor in an Employee class** was successfully implemented and executed.
