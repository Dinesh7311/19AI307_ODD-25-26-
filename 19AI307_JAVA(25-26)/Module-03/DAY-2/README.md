# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program using method overloading to print student details. Create a class Student with:

## AIM:
To develop a Java program that uses method overloading to print student details by creating a Student class with multiple methods to display different sets of student information.

## ALGORITHM :
1.Start

2.Read three names, two ages, and one department from the user

3.Create a Student object

4.Call print(name) to display only the name

5.Call print(name, age) to display name and age

6.Call print(name, age, dept) to display full details

7.End

## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by:DINESH S 
RegisterNumber:212224240038  
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
class Student 
{
    void print(String name)
    {
        System.out.println("Name: " + name);
    }
    void print(String name, int age)
    {
        System.out.println("Name: " + name + ", Age: " + age);
    }
    void print(String name, int age, String dept)
    {
        if(age==20)
        {
            System.out.println("Name: " + name + ", Age: " + age + ", Dept: "+ dept);
        }
        else
        {
            System.out.println("Name: " + name + " , Age: " + age + ", Dept: "+ dept);
        }
    }
    
}    
public class Main 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        String name1 = sc.nextLine().trim();
        String name2 = sc.nextLine().trim();
        int age = Integer.parseInt(sc.nextLine().trim());
        String name3 = sc.nextLine().trim();
        int age2 = Integer.parseInt(sc.nextLine().trim());
        String dept = sc.nextLine().trim();
        Student s = new Student();
        s.print(name1);
        s.print(name2, age);
        s.print(name3, age2, dept);
    }
}
```
## OUTPUT:

<img width="973" height="745" alt="image" src="https://github.com/user-attachments/assets/f562f448-b0f7-4ef4-8abb-a570c34b69ba" />



## RESULT:
The program reads student details and displays them using method overloading with different versions of the print() method.
