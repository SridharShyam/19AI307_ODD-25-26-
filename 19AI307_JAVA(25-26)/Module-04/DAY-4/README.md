# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
```
You’re creating a cross-platform UI tool using the Abstract Factory pattern. Implement factories to create Button and Checkbox for "dark" and "light" themes. Let the user choose the theme, then generate UI components and display their types
```

## AIM:
To develop a Java program that demonstrates the **Abstract Factory Design Pattern** by creating UI components (`Button` and `Checkbox`) for different themes (`Dark` and `Light`) based on user input.

## ALGORITHM :
1. Start the program.
2. Import the necessary package `java.util.Scanner` to read input from the user.
3. Create an interface `Button` with a method `createButton()`.
4. Create an interface `Checkbox` with a method `createCheckbox()`.
5. Implement `Button` interface in classes `DarkButton` and `LightButton`.
6. Implement `Checkbox` interface in classes `DarkCheckbox` and `LightCheckbox`.
7. Create an interface `UIFactory` with methods `createButton()` and `createCheckbox()`.
8. Create a class `DarkThemeFactory` that implements `UIFactory` and returns `DarkButton` and `DarkCheckbox`.
9. Create a class `LightThemeFactory` that implements `UIFactory` and returns `LightButton` and `LightCheckbox`.
10. Create a class `Main` containing the `main()` method.
11. Use a `Scanner` object to read the theme input from the user.
12. Based on the input, instantiate either `DarkThemeFactory` or `LightThemeFactory`.
13. Use the factory to create `Button` and `Checkbox` objects.
14. Call the respective methods to display the created UI components.
15. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: 
RegisterNumber:  
*/

import java.util.Scanner;

// Button Interface
interface Button {
    void createButton();
}

// Checkbox Interface
interface Checkbox {
    void createCheckbox();
}

// Dark Button
class DarkButton implements Button {
    public void createButton() {
        System.out.println("Dark Button created");
    }
}

// Light Button
class LightButton implements Button {
    public void createButton() {
        System.out.println("Light Button created");
    }
}

// Dark Checkbox
class DarkCheckbox implements Checkbox {
    public void createCheckbox() {
        System.out.println("Dark Checkbox created");
    }
}

// Light Checkbox
class LightCheckbox implements Checkbox {
    public void createCheckbox() {
        System.out.println("Light Checkbox created");
    }
}

// Abstract Factory
interface UIFactory {
    Button createButton();
    Checkbox createCheckbox();
}

// Dark Theme Factory
class DarkThemeFactory implements UIFactory {
    public Button createButton() {
        return new DarkButton();
    }

    public Checkbox createCheckbox() {
        return new DarkCheckbox();
    }
}

// Light Theme Factory
class LightThemeFactory implements UIFactory {
    public Button createButton() {
        return new LightButton();
    }

    public Checkbox createCheckbox() {
        return new LightCheckbox();
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String theme = sc.nextLine();

        UIFactory factory;

        if(theme.equalsIgnoreCase("dark")) {
            factory = new DarkThemeFactory();
        } 
        else if(theme.equalsIgnoreCase("light")) {
            factory = new LightThemeFactory();
        } 
        else {
            System.out.println("Invalid theme");
            return;
        }

        Button button = factory.createButton();
        Checkbox checkbox = factory.createCheckbox();

        button.createButton();
        checkbox.createCheckbox();
    }
}
```
## OUTPUT:

<img width="547" height="267" alt="image" src="https://github.com/user-attachments/assets/e34c2c9d-e357-481c-92cf-decb7fc8d749" />

## RESULT:
Thus, the Java program demonstrating the **Abstract Factory Design Pattern to create themed UI components (Button and Checkbox)** was successfully implemented and executed.
