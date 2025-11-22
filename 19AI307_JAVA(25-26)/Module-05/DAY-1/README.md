# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a Java program to write text into a file using FileOutputStream.

## AIM:
To write a Java program that demonstrates how to create a file and write text into it using the FileOutputStream class.

## ALGORITHM :
1.Read the file name.

2.Read the text to write.

3.Create FileOutputStream for the file.

4.Convert text to bytes and write to file.

5.Close the stream.

6.Print success message or error if exception occurs.


## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by:DINESH S 
RegisterNumber: 212224240038 
*/
```

## SOURCE CODE:
```
import java.io.FileOutputStream;
import java.io.IOException;
import java.util.Scanner;

public class WriteUsingFOS {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String fileName = scanner.nextLine();

        String content = scanner.nextLine();

        try {
            FileOutputStream fos = new FileOutputStream(fileName);

            fos.write(content.getBytes());

            fos.close();

            System.out.println("File written successfully.");
        } catch (IOException e) {
            System.out.println("An error occurred.");
        }

        scanner.close();
    }
}
```

## OUTPUT:

<img width="1117" height="482" alt="image" src="https://github.com/user-attachments/assets/50b7ce72-27af-4833-9d89-b40ec8ef9067" />


## RESULT:
The program successfully writes the given text into the specified file and displays the message "File written successfully.
