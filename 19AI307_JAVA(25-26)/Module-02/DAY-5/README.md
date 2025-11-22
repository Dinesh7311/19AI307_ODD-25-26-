# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Write a method that accepts a string and returns whether it contains only lowercase letters or not.

## AIM:
To write a method that checks a given string and determines whether it contains only lowercase letters.

## ALGORITHM :
1.Start the program.
2.Read a string input from the user.
3.Create a method isAllLowercase() that takes the string as input.
4.Loop through each character of the string.
5.Check if every character is between 'a' and 'z'.
6.If any character is not lowercase, return false.
7.If all characters are lowercase, return true.
8.Print the returned result.
9.End the program.

## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by:DINESH S
RegisterNumber:212224240038 
*/
```

## SOURCE CODE:
```

import java.util.Scanner;
class prog 
{
    public static boolean isAllLowercase(String input) 
    {
        for(int i=0;i<input.length();i++)
        {
            char ch=input.charAt(i);
            if(!(ch>='a' && ch <='z'))
            {
                return false;
            }
        }
        return true;
        // Your Logic Here
    }

    public static void main(String[] args) 
    {
        Scanner scanner = new Scanner(System.in);
        String str = scanner.nextLine();
        System.out.println(isAllLowercase(str));
        // Call the method and display result
        scanner.close();
    }
}
```
## OUTPUT:


<img width="533" height="444" alt="image" src="https://github.com/user-attachments/assets/8a8f53ee-4206-4080-86fb-fddd4a2c2779" />


## RESULT:
The program checks the given string and displays whether it contains only lowercase letters or not.
