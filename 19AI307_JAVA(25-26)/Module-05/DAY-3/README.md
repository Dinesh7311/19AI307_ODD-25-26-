# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Read a file and print only the lines containing the word "Java".

## AIM:
To write a Java program that reads a file and displays only the lines that contain the word "Java".

## ALGORITHM :
1.Read user input.

2.Create PipedOutputStream and connect to PipedInputStream.

3.Create and start WriterThread to write data to the pipe.

4.Create and start ReaderThread to read data from the pipe.

5.WriterThread writes bytes and closes stream.

6.ReaderThread reads bytes, converts to string, and prints.

7.End.





## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: DINESH S
RegisterNumber:212224240038  
*/
```

## SOURCE CODE:
```
import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;

public class JavaLineFilter {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        List<String> linesWithJava = new ArrayList<>();
        while (true) {
            String line = scanner.nextLine();
            if (line.equalsIgnoreCase("exit")) {
                break;
            }
            if (line.contains("Java")) 
            { 
                linesWithJava.add(line);
            }
        }
        
        System.out.println("Lines containing the word 'Java':");
        for (String javaLine : linesWithJava) {
            System.out.println(javaLine);
        }
        
        scanner.close();
    }
}
```

## OUTPUT:
<img width="1260" height="484" alt="image" src="https://github.com/user-attachments/assets/95906ee6-4387-4197-aa0e-95ea8fd0f634" />

## RESULT:
The program transfers user input from one thread to another using piped streams and displays the received message.

