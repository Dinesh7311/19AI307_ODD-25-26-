# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program to convert a string to an integer using a wrapper class and perform addition.

## AIM:
To develop a Java program that converts strings into integers using the Integer wrapper class and performs addition on the converted values.

## ALGORITHM :
1.Algorithm (Short):

2.Read two strings

3.Convert both strings to integers

4.Add the two integers

5.Print the sum

6.End





## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by:DINESH S 
RegisterNumber:212224240038 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
public class StringToIntegerAddition
{
    public static void main(String[] args) 
    {
        Scanner scanner = new Scanner(System.in);
        String str1 = scanner.nextLine();
        String str2 = scanner.nextLine();
        int n = Integer.parseInt(str1);
        int m = Integer.parseInt(str2);
        int sum = n + m;
        System.out.println("Sum = " + sum);
        scanner.close();
    }
}
```

## OUTPUT:

<img width="666" height="488" alt="image" src="https://github.com/user-attachments/assets/e304aeff-4635-4724-a49b-f65a68eaa857" />



## RESULT:
The program converts two input strings into integers, adds them, and prints the sum.
