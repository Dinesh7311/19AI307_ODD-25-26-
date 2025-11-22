# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
You wrote a program that stores some input strings into a String array and prints each string in uppercase. However, you're getting a NullPointerException. What should you check in your array before calling .toUpperCase() on a element?

## AIM:
To understand how to avoid a NullPointerException by checking whether an array element is null before calling .toUpperCase() on it.

## ALGORITHM :
1.Start

2.Read a string input

3.Check if the input is null or the text "null"

4.If yes → print "Null element"

5.Else → convert the string to uppercase and print it

6.End





## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by:DINESH S
RegisterNumber: 212224240038 
*/
```

## SOURCE CODE:
```

import java.util.Scanner;

public class UppercaseArrayExample {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String input = scanner.nextLine();
        scanner.close();

        if (input == null || input.equalsIgnoreCase("null")) {
            System.out.println("Null element");
        } else {
            System.out.println(input.toUpperCase());
        }
    }
}
```
## OUTPUT:
<img width="774" height="416" alt="image" src="https://github.com/user-attachments/assets/cc88e209-36ff-4331-b28a-a29182a2ee43" />



## RESULT:
The program checks whether the input is null and prints “Null element”; otherwise, it prints the input in uppercase.
