# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
```
Write a Java program to serialize a collection of objects (like ArrayList<Student>) into a file.
```

## AIM:
To develop a Java program that demonstrates **serialization and deserialization** by storing a collection of `Student` objects (`ArrayList<Student>`) into a file and retrieving them back.


## ALGORITHM :
1. Start the program.
2. Import the necessary packages `java.io.*` and `java.util.*`.
3. Create a class `Student` that implements the `Serializable` interface.
4. Declare instance variables `id`, `name`, and `marks`.
5. Create a constructor to initialize student details.
6. Override the `toString()` method to display student information.
7. Create a method `serializeStudents()` to write the list of students into a file using `ObjectOutputStream`.
8. Create a method `deserializeStudents()` to read the list of students from the file using `ObjectInputStream`.
9. Create a class containing the `main()` method.
10. Create a `Scanner` object to read input from the user.
11. Read the number of students `n`.
12. Loop `n` times to read student details (id, name, marks).
13. Store each student object in an `ArrayList`.
14. Call the `serializeStudents()` method to store the data into a file.
15. Call the `deserializeStudents()` method to retrieve the data from the file.
16. Display the deserialized student details.
17. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: SHYAM S
RegisterNumber: 212223240156
*/

import java.io.*;
import java.util.*;

// Student class must implement Serializable
class Student implements Serializable {
    private static final long serialVersionUID = 1L;

    private int id;
    private String name;
    private double marks;

    public Student(int id, String name, double marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    @Override
    public String toString() {
        return "Student{id=" + id + ", name='" + name + "', marks=" + marks + "}";
    }
}

public class StudentSerializationUserInput {

    // Serialize list of students
    public static void serializeStudents(List<Student> students, String fileName) {
        try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(fileName))) {
            oos.writeObject(students);
            System.out.println("Students serialized successfully into: " + fileName);
        } catch (IOException e) {
            System.out.println("Error during serialization: " + e.getMessage());
        }
    }

    // Deserialize list of students
    @SuppressWarnings("unchecked")
    public static List<Student> deserializeStudents(String fileName) {
        List<Student> students = null;
        try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream(fileName))) {
            students = (List<Student>) ois.readObject();
            System.out.println("Students deserialized successfully from: " + fileName);
        } catch (IOException | ClassNotFoundException e) {
            System.out.println("Error during deserialization: " + e.getMessage());
        }
        return students;
    }

    public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in);
    List<Student> students = new ArrayList<>();

    int n = scanner.nextInt();
    scanner.nextLine(); // consume newline

    // Read student details
    // Write your code here
    for (int i = 0; i < n; i++) {
        int id = scanner.nextInt();
        scanner.nextLine();
        String name = scanner.nextLine();
        double marks = scanner.nextDouble();
        scanner.nextLine();
        students.add(new Student(id, name, marks));
    }

    String fileName = "students.dat";

    // Serialize students
    serializeStudents(students, fileName);

    // Deserialize students
    List<Student> deserializedStudents = deserializeStudents(fileName);

    // Display deserialized data
    if (deserializedStudents != null) {
        System.out.println("\nDeserialized Students:");
        for (Student s : deserializedStudents) {
            System.out.println(s);
        }
    }

    scanner.close();
}
}

```
## OUTPUT:

<img width="1183" height="825" alt="image" src="https://github.com/user-attachments/assets/49f0ba5e-17cc-4acd-b2e8-576ed47df91e" />

## RESULT:
Thus, the Java program demonstrating **serialization and deserialization of a collection of Student objects using file handling** was successfully implemented and executed.
