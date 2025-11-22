# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Print Right-Angled Triangle Star Pattern

## AIM:
To write a program that prints a right-angled triangle star pattern, where the number of rows is determined by user input.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	For each row i from 1 to n:
4. For each column j from 1 to i: 
5. Print "* " (without moving to a new line).
6.Move to the next line after printing all stars in the current row. 
7.End

## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: DINESH S
RegisterNumber:212224240038
*/
```

## SOURCE CODE:
```
import java.util.*;
public class RightAngledTriangle
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt(); 
        for (int i = 1; i <= n; i++)
        {
            for (int j = 1; j <= i; j++)
            {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}
```





## OUTPUT:

<img width="571" height="440" alt="image" src="https://github.com/user-attachments/assets/72023044-eba9-404d-9ea7-c8dd3d4b6936" />


## RESULT:
Thus, the given program executes successfully, and the output matches the expected pattern for a right-angled triangle, verifying that the stars are printed correctly row by row.

