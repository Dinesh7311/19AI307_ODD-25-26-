# Ex.No:2(B) METHODS

## QUESTION:
Write a method int cube(int x) that calls a method int square(int x) internally to calculate the cube as x * square(x).

## AIM:
To write a Java program that calculates the cube of a number using a cube(int x) method which internally calls the square(int x) method.

## ALGORITHM :
1.Start.

2.Read a number.

3.Calculate square using square(x).

4.Calculate cube using cube(x) which calls square(x).

5.Print the result.

6.End.




## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by:DINESH S
RegisterNumber:212224240038  
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class MathUtil {
    // Method to calculate square
    int square(int x) {
        return x * x;
    }

    // Method to calculate cube using square()
    int cube(int x) {
        return x * square(x);
    }
}

class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int num = sc.nextInt();

        MathUtil util = new MathUtil();
        int result = util.cube(num);

        System.out.println(result);

        sc.close();
    }
}
```

## OUTPUT:


<img width="555" height="256" alt="image" src="https://github.com/user-attachments/assets/bfe6a96b-8324-4032-9397-495f2ff7318e" />


## RESULT:
The program successfully calculated the cube of the given number using the square() method internally.
