# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java program to find the sum of even and odd elements in an array

## AIM:
To write a Java program that calculates and displays the sum of even and odd elements separately in a given array.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.Declare an integer array of size n.
4.Input all n elements into the array.
5.Initialize two variables ev and od to 0 (to store sums of even and odd elements).
6.For each element in the array:
7.If the element is divisible by 2 (even) → Add it to ev.
8.Else (odd) → Add it to od. 9.End





## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: DINESH S
RegisterNumber:212224240038
*/
```

## SOURCE CODE:

```
import java.util.*;
public class main
{
    static public void main(String[] args)
    {
        Scanner o=new Scanner(System.in);
        int n=o.nextInt();
        int [] arr = new int[n];
        for(int i=0; i<n; i++)
        {
            arr[i]=o.nextInt();
        }
        int ev=0, od=0;
        for(int i=0;i<n;i++)
        {
            if(arr[i]%2==0)
            {
                ev+=arr[i];
            }
            else
            {
                od+=arr[i];
            }
        }
        System.out.println("Sum of even elements: " + ev);
        System.out.println("Sum of odd elements: "+ od);
    }
}
```





## OUTPUT:

<img width="782" height="734" alt="image" src="https://github.com/user-attachments/assets/966a0a56-15ec-4a00-98cf-802a2539b319" />


## RESULT:

Thus, the program executes successfully and correctly calculates the sum of even and odd elements in the array as expected.
