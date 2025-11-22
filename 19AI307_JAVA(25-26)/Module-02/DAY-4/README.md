# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a class that uses a constructor to initialize variables and overrides toString() method.

## AIM:
To initialize variables using a constructor and display them using an overridden toString() method.

## ALGORITHM :
1.Start the program.

2.Define a Student class with private variables name and age.

3.Create a constructor to initialize these variables.

4.Override the toString() method to return student details as a string.

5.In the main method, read the name and age from the user.

6.Create a Student object using the constructor.

7.Print the object, which automatically calls the toString() method.

8.End the program.

## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: DINESH S
RegisterNumber:212224240038  
*/
```

## SOURCE CODE:
```

import java.util.Scanner;

class Student {
    private String name;
    private int age;

    public Student(String name, int age) {
        this.name = name;
        this.age = age;
    }

    @Override
    public String toString() {
        return "Student{name='" + name + "', age=" + age + "}";
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String name = sc.nextLine();
        int age = sc.nextInt();
        Student s = new Student(name, age);
        System.out.println(s);
        sc.close();
    }
}
```

## OUTPUT:

<img width="937" height="485" alt="image" src="https://github.com/user-attachments/assets/56e70941-b096-4799-af05-49653fbb7c02" />
## RESULT:
The program creates a student object and prints its details using toString().
