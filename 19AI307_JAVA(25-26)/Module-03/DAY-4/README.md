# Ex.No:3(D)    INTERFACE 

## QUESTION:
You are programming bots that analyze weather data. Each bot must implement a common interface and give a prediction.

## AIM:
To create weather-analysis bots that follow a common interface and generate predictions based on the given weather data.

## ALGORITHM :
1.Start

2.Read temperature

3.Read bot type (1 = SunBot, 2 = RainBot)

4.If bot type is 1 → create SunBot

5.Else if bot type is 2 → create RainBot

6.Else → print "Invalid bot type" and stop

7.Call predict(temperature) on the selected bot

8.End

## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by:DINESH S
RegisterNumber:212224240038 
*/
```

## SOURCE CODE:
```
import java.util.*;

interface WeatherBot {
    void predict(int temperature);
}

class SunBot implements WeatherBot {
    public void predict(int temperature) {
        if (temperature > 30) {
            System.out.println("HOT");
        } else {
            System.out.println("MODERATE");
        }
    }
}

class RainBot implements WeatherBot {
    public void predict(int temperature) {
        if (temperature < 20) {
            System.out.println("COLD");
        } else {
            System.out.println("WARM");
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int temperature = sc.nextInt();
        int botType = sc.nextInt();

        WeatherBot bot;

        if (botType == 1) {
            bot = new SunBot();
        } else if (botType == 2) {
            bot = new RainBot();
        } else {
            System.out.println("Invalid bot type");
            sc.close();
            return;
        }

        bot.predict(temperature);
        sc.close();
    }
}
```
## OUTPUT:

<img width="569" height="315" alt="image" src="https://github.com/user-attachments/assets/8952b61b-dc7f-4f5f-9e12-25f11bbc0a20" />



## RESULT:
The program selects the appropriate weather bot based on user input and prints a prediction using the given temperature.
