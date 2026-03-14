# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
```
A fuel station sells two types of fuels: Petrol and Diesel.

There is a base class named Fuel, which has the following attributes: fuelId (a string representing the fuel transaction ID), customerName (the name of the customer), litersPurchased (the quantity of fuel bought in liters), and pricePerLiter (the cost of one liter of the fuel).

Two classes, Petrol and Diesel, inherit from the Fuel class. The Petrol class applies a 3% discount on the total bill amount, whereas the Diesel class applies a 5% discount on the total bill amount.

Your task is to write a program that accepts exactly three fuel purchase records. Each record starts with the fuel type (either Petrol or Diesel), followed by the fuelId, customerName, litersPurchased, and pricePerLiter.

For each record, the program should calculate the total price after applying the respective discount and display the details of the purchase, including the discount rate and the final amount payable.

The input format for each record is as follows:

Fuel type (Petrol or Diesel)

fuelId (String)

customerName (String)

litersPurchased (double)

pricePerLiter (double)

The program should process exactly three such inputs and output the complete details for each purchase.

import java.util.Scanner;
import java.text.DecimalFormat;

class Fuel {
    String fuelId, customerName;
    double litersPurchased, pricePerLiter;

    Fuel(String fuelId, String customerName, double litersPurchased, double pricePerLiter) {
        this.fuelId = fuelId;
        this.customerName = customerName;
        this.litersPurchased = litersPurchased;
        this.pricePerLiter = pricePerLiter;
    }

    double getDiscountRate() {
        return 0;
    }

    double calculateTotalPrice() {
        double total = litersPurchased * pricePerLiter;
        double discountAmount = total * getDiscountRate() / 100;
        return total - discountAmount;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Fuel ID: " + fuelId);
        System.out.println("Customer Name: " + customerName);
        System.out.println("Fuel Type: General");
        System.out.println("Liters Purchased: " + litersPurchased);
        System.out.println("Price per Liter: " + pricePerLiter);
        System.out.println("Discount: " + getDiscountRate() + "%");
        System.out.println("Total Price: " + df.format(calculateTotalPrice()));
       
    }
}
```

## AIM:
To develop a Java program that demonstrates **inheritance** by creating a base class `Fuel` and derived classes `Petrol` and `Diesel`, where each derived class applies a specific discount rate and calculates the final fuel purchase amount.

## ALGORITHM :
1. Start the program.
2. Import the necessary packages `java.util.Scanner` and `java.text.DecimalFormat`.
3. Create a base class named `Fuel`.
4. Declare instance variables `fuelId`, `customerName`, `litersPurchased`, and `pricePerLiter`.
5. Create a constructor in the `Fuel` class to initialize these variables.
6. Define a method `getDiscountRate()` that returns the discount percentage.
7. Define a method `calculateTotalPrice()` to compute the total price after applying the discount.
8. Define a method `display()` to print the fuel purchase details.
9. Create a class `Petrol` that extends the `Fuel` class.
10. Override the `getDiscountRate()` method to return **3% discount** for petrol.
11. Override the `display()` method to show the fuel type as Petrol.
12. Create another class `Diesel` that extends the `Fuel` class.
13. Override the `getDiscountRate()` method to return **5% discount** for diesel.
14. Override the `display()` method to show the fuel type as Diesel.
15. Create the `Main` class containing the `main()` method.
16. Use a `Scanner` object to read the fuel type, fuel ID, customer name, liters purchased, and price per liter.
17. Based on the fuel type entered, create an object of `Petrol`, `Diesel`, or `Fuel`.
18. Call the `display()` method to print the purchase details including discount and final price.
19. Stop the program.
## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: SHYAM S
Register Number: 212223240156
*/

import java.util.Scanner;
import java.text.DecimalFormat;

class Fuel {
    String fuelId, customerName;
    double litersPurchased, pricePerLiter;

    Fuel(String fuelId, String customerName, double litersPurchased, double pricePerLiter) {
        this.fuelId = fuelId;
        this.customerName = customerName;
        this.litersPurchased = litersPurchased;
        this.pricePerLiter = pricePerLiter;
    }

    double getDiscountRate() {
        return 0;
    }

    double calculateTotalPrice() {
        double total = litersPurchased * pricePerLiter;
        double discountAmount = total * getDiscountRate() / 100;
        return total - discountAmount;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Fuel ID: " + fuelId);
        System.out.println("Customer Name: " + customerName);
        System.out.println("Fuel Type: General");
        System.out.println("Liters Purchased: " + litersPurchased);
        System.out.println("Price per Liter: " + pricePerLiter);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Total Price: " + df.format(calculateTotalPrice()));
       
    }
}

class Petrol extends Fuel
{
    Petrol(String fuelId, String customerName, double litersPurchased, double pricePerLiter)
    {
        super(fuelId, customerName, litersPurchased, pricePerLiter);
    }
    double getDiscountRate()
    {
        return 3;
    }
    void display()
    {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Fuel ID: " + fuelId);
        System.out.println("Customer Name: " + customerName);
        System.out.println("Fuel Type: Petrol");
        System.out.println("Liters Purchased: " + litersPurchased);
        System.out.println("Price per Liter: " + pricePerLiter);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Total Price: " + df.format(calculateTotalPrice()));
       
    }
}

class Diesel extends Fuel
{
    Diesel(String fuelId, String customerName, double litersPurchased, double pricePerLiter)
    {
        super(fuelId, customerName, litersPurchased, pricePerLiter);
    }
    double getDiscountRate()
    {
        return 5;
    }
    void display()
    {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Fuel ID: " + fuelId);
        System.out.println("Customer Name: " + customerName);
        System.out.println("Fuel Type: Diesel");
        System.out.println("Liters Purchased: " + litersPurchased);
        System.out.println("Price per Liter: " + pricePerLiter);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Total Price: " + df.format(calculateTotalPrice()));
    }
}

public class Main
{
    public static void main(String args[])
    {
        Scanner scan=new Scanner(System.in);
        
        String fuelType=scan.nextLine().trim();
        String fuelId=scan.nextLine();
        String customerName=scan.nextLine();
        double litersPurchased=scan.nextDouble();
        double pricePerLiter=scan.nextDouble();
        Fuel f;
        if(fuelType.equalsIgnoreCase("Petrol"))
        {
            f=new Petrol(fuelId, customerName, litersPurchased, pricePerLiter);
        }
        else if(fuelType.equalsIgnoreCase("Diesel"))
        {
            f=new Diesel(fuelId, customerName, litersPurchased, pricePerLiter);
        }
        else
        {
            f=new Fuel(fuelId, customerName, litersPurchased, pricePerLiter);
        }
        f.display();
    }
}
```

## OUTPUT:



## RESULT:
Thus, the Java program demonstrating **inheritance using Fuel, Petrol, and Diesel classes to calculate discounted fuel prices** was successfully implemented and executed.
