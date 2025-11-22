# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called Person with private instance variables name, age. and country. Provide public getter and setter methods to access and modify these variables.

## AIM:
To create a Person class with private variables and provide public getter and setter methods to access and modify them.

## ALGORITHM :
1.Start the program.

2.Read name, age, and country from the user.

3.Create a Person object.

4.Set the values using setter methods.

5.Display the values using getter methods.

6.End the program.


## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by:DINESH S
RegisterNumber:212224240038  
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class Person {
    private String name;
    private int age;
    private String country;

    public String getName() {
        return name;
    }
    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }
    public void setAge(int age) {
        this.age = age;
    }

    public String getCountry() {
        return country;
    }
    public void setCountry(String country) {
        this.country = country;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String name = sc.nextLine();
        int age = sc.nextInt();
        sc.nextLine(); // consume leftover newline
        String country = sc.nextLine();

        Person p = new Person();
        p.setName(name);
        p.setAge(age);
        p.setCountry(country);
        System.out.println("Person 1");
        System.out.println("Name: " + p.getName());
        System.out.println("Age: " + p.getAge());
        System.out.println("Country: " + p.getCountry());

        sc.close();
    }
}
```

## OUTPUT:


<img width="817" height="563" alt="image" src="https://github.com/user-attachments/assets/4d33239b-def2-4f6a-be5e-acad502a50f1" />


## RESULT:
The program displays the entered name, age, and country of the person.
