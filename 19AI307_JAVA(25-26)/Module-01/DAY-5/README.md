# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a Java program to reverse a given string.

## AIM:
To write a Java program that takes a string as input and prints its reverse.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.Create a StringBuilder object with the input string.
4.Use the reverse() method of StringBuilder to reverse the string.
5.Convert the reversed StringBuilder back to a string.
6.Print the reversed string.
7.End





## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: DINESH S
RegisterNumber:212224240038
*/
```

## SOURCE CODE:
```
import java.util.*;
public class main
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        String str = sc.nextLine();
        String reversed = new StringBuilder(str).reverse().toString();
        System.out.println("Reversed string: " + reversed);
    }
}
```

## OUTPUT:
<img width="771" height="372" alt="image" src="https://github.com/user-attachments/assets/24e19dbc-d60a-465e-856a-0845f9a19ada" />


## RESULT:
Thus, the program executes successfully and correctly reverses the input string, displaying the expected output.
