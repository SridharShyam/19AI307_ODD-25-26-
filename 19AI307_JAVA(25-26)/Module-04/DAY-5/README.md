# Ex.No:4(D) DESIGN PATTERN  -- MEMENTO PATTERN

## QUESTION:
```
Create a class Note that stores a note content. Allow saving multiple versions and restoring a previous one. (Memento Pattern)
```

## AIM:

To develop a Java program that demonstrates the **Memento Design Pattern** by creating a `Note` class that allows saving multiple versions of its content and restoring a previous version.

## ALGORITHM:
1. Start the program.
2. Import the necessary package `java.util.*` to use `Scanner` and `ArrayList`.
3. Create a class `Note` to store the content of the note.
4. Provide setter and getter methods to modify and access the content.
5. Create a class `NoteMemento` to store a snapshot of the note content.
6. Define a constructor in `NoteMemento` to save the content.
7. Create a method to return the saved content.
8. Create a class `NoteHistory` to manage saved versions of notes.
9. Declare a list to store multiple `NoteMemento` objects.
10. Create a method `saveVersion()` to store the current state of the note.
11. Create a method `restoreVersion(int index)` to retrieve a saved version.
12. Create a class `NoteManager` containing the `main()` method.
13. Use a `Scanner` object to read input from the user.
14. Read the number of versions `n`.
15. Loop `n` times to read note contents and save each version.
16. Read the index of the version to restore.
17. Retrieve and display the selected version using `restoreVersion()`.
18. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: SHYAM S
RegisterNumber: 212223240156
*/

import java.util.*;

class Note {
    private String content;

    // Setter
    public void setContent(String content) {
        this.content = content;
    }

    // Getter
    public String getContent() {
        return content;
    }
}

class NoteMemento {
    private String content;

    // Store content snapshot
    public NoteMemento(String content) {
        this.content = content;
    }

    public String getSavedContent() {
        return content;
    }
}

class NoteHistory {
    private List<NoteMemento> history = new ArrayList<>();

    // Save version
    public void saveVersion(Note note) {
        history.add(new NoteMemento(note.getContent()));
    }

    // Restore version
    public String restoreVersion(int index) {
        return history.get(index).getSavedContent();
    }
}

public class NoteManager {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Note note = new Note();
        NoteHistory history = new NoteHistory();

        int n = sc.nextInt();
        sc.nextLine();

        // Read and save versions
        for (int i = 0; i < n; i++) {
            String version = sc.nextLine();
            note.setContent(version);
            history.saveVersion(note);
        }

        // Version to restore
        int restoreIndex = sc.nextInt();

        // Print restored content
        System.out.println(history.restoreVersion(restoreIndex));

        sc.close();
    }
}
```
## OUTPUT:

<img width="1052" height="533" alt="image" src="https://github.com/user-attachments/assets/1a5ff68c-aefd-4c72-abfa-1f9aab64449a" />

## RESULT:
Thus, the Java program demonstrating the **Memento Design Pattern to save and restore multiple versions of a note** was successfully implemented and executed.
