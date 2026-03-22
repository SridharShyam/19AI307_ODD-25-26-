# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
```
Implement a system where a Library contains multiple Book objects. Each Book is created inside the Library. Books can't exist independently (Composition).
```
## AIM:

To develop a Java program that demonstrates **composition** by creating a `Library` class that contains multiple `Book` objects, where the `Book` objects are created and managed within the `Library` and cannot exist independently.

## ALGORITHM :
1. Start the program.
2. Import the necessary package `java.util.*` to use `Scanner` and `ArrayList`.
3. Create a class named `Book`.
4. Declare private variables `title` and `author`.
5. Create a constructor to initialize the book details.
6. Define a method `getDetails()` to return the book information.
7. Create a class named `Library`.
8. Declare a list `books` to store multiple `Book` objects.
9. Create a method `addBook(String title, String author)` to create and add a `Book` object to the list.
10. Create a method `showBooks()` to display all book details.
11. Create a class `CompositionExample` containing the `main()` method.
12. Create a `Scanner` object to read input from the user.
13. Read the number of books `n`.
14. Loop `n` times to read book title and author.
15. Add each book to the library using the `addBook()` method.
16. Call `showBooks()` to display all stored books.
17. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: SHYAM S
RegisterNumber: 212223240156
*/

import java.util.*;

public class CompositionExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Library library = new Library();

        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String title = sc.nextLine();
            String author = sc.nextLine();
            library.addBook(title, author);
        }

        library.showBooks();
        sc.close();
    }
}

class Book {
    private String title;
    private String author;

    public Book(String title, String author) {
        this.title = title;
        this.author = author;
    }

    public String getDetails() {
        return title + " by " + author;
    }
}

class Library {
    
    private List<Book> books = new ArrayList<>();

    public void addBook(String title, String author) {
        // Type Your Code Here
        books.add(new Book(title, author));
    }

    public void showBooks() {
        // Type Your Code Here
        System.out.println("Books in Library:");
        for(Book b:books)
        {
            System.out.println("- "+b.getDetails());
        }
    }
}
```

## OUTPUT:

<img width="798" height="483" alt="image" src="https://github.com/user-attachments/assets/dc744c8a-8a4d-4147-9d8b-a48cdb855f90" />

## RESULT:
Thus, the Java program demonstrating **composition by creating a Library class that manages Book objects internally** was successfully implemented and executed.
