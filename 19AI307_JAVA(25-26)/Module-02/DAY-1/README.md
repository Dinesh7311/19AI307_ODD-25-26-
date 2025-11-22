# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class City with attributes: cityName (String), population (long), area (double). Create an object. Print all details.

## AIM:
To write a Java program that creates a class City with attributes cityName, population, and area, then creates an object of the class and prints all the details of the city.

## ALGORITHM :
1.Start.

2.Create a class City with variables: cityName, population, area.

3.Add a method printDetails() to display the values.

4.In main(), create a Scanner object.

5.Create a City object.

6.Read city name, population, and area from the user.

7.Call printDetails() to print the details.

8.End.




## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: DINESH S
RegisterNumber:212224240038 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class City {
    String cityName;
    long population;
    double area;

    // Method to print details
    void printDetails() {
        System.out.println("City Name: " + cityName);
        System.out.println("Population: " + population);
        System.out.println("Area: " + area);
    }
}

class prog {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Create a City object
        City city = new City();

        // Read details from user
        city.cityName = scanner.nextLine();    // Read city name
        city.population = scanner.nextLong();  // Read population
        city.area = scanner.nextDouble();      // Read area

        // Print city details
        city.printDetails();

        scanner.close();
    }
}
```

## OUTPUT:

<img width="743" height="478" alt="image" src="https://github.com/user-attachments/assets/1b03a826-185f-4dcb-9873-12fbf459bdd7" />



## RESULT:
The program successfully created a City object and displayed its details.
