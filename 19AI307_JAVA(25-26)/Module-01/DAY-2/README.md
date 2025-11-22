# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
In a haunted house, lights turn on or off based on the hour of entry: If the hour is even and between 2 and 6 (inclusive), lights flicker. If the hour is odd and between 7 and 11, lights stay off. If the hour is 12, lights turn red. Otherwise, the house is dark. The program will print one of the following statements based on the input: Lights flicker Lights off Lights red Dark house

## AIM:
To create a program that simulates the lighting behavior of a haunted house, determining whether the lights flicker, stay off, turn red, or the house remains dark based on the hour of entry.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Input the hour of entry n (an integer between 1 and 12). 
4.Check if n is even:
5.If yes: If n is between 2 and 6 (inclusive) → Print "Lights flicker". Else if n is 12 → Print "Lights red".
6.Else → Print "Dark house".
7.If n is odd: If n is between 7 and 11 (inclusive) → Print "Lights off". Else → Print "Dark house".
8.End
## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: DINESH S
RegisterNumber:212224240038
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Main
{
    public static void main(String[] args)
    {
        Scanner o = new Scanner(System.in);
        int n = o.nextInt();
        if (n % 2 == 0)
        {   
            if (n >= 2 && n <= 6)
            {
                System.out.print("Lights flicker");
            } 
            else if (n == 12) 
            {
                System.out.print("Lights red");
            }
            else
            {
                System.out.print("Dark house");
            }
        } 
        else
        {   
            if (n >= 7 && n <= 11)
            {
                System.out.print("Lights off");
            } 
            else
            {
                System.out.print("Dark house");
            }
        }
    }
}
```






## OUTPUT:
<img width="929" height="358" alt="image" src="https://github.com/user-attachments/assets/a4898f69-eea7-4bac-a51f-6839eeec556c" />

## RESULT:
Thus, the given program executes successfully, and the output matches the expected results for different hours of entry, verifying that the haunted house lighting behavior is correctly simulated..
