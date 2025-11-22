# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
You are designing a microservices-based system where multiple services like AuthService, UserService, OrderService, etc., need to log important system events.

## AIM:
To design a microservices system where multiple services can log important events consistently using a common logging mechanism.

## ALGORITHM :
1.Start

2.Read number of log entries n

3.For each entry:
     . Read service, level, and message
     . Get Logger instance
     . Add the log
     . Print current logs
4.End




## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: DINESH S
RegisterNumber: 212224240038 
*/
```

## SOURCE CODE:
```
import java.util.*;

class Logger {
    private static Logger instance = null;
    private List<String> logs;

    private Logger() {
        logs = new ArrayList<>();
    }

    public static Logger getInstance() {
        if (instance == null) {
            instance = new Logger();
        }
        return instance;
    }

    
    public void addLog(String service, String level, String message) {
        String logMessage = service + " " + level + ": " + message;
        logs.add(logMessage);

        System.out.println(logMessage);
        System.out.println("Current Logs:");
        for (int i = 0; i < logs.size(); i++) {
            System.out.println((i + 1) + ". " + logs.get(i));
        }
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt(); 
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String[] input = sc.nextLine().split(" ");
            String service = input[0];
            String level = input[1];
            String message = input[2];

            Logger logger = Logger.getInstance();
            logger.addLog(service, level, message);
            System.out.println();
        }
        sc.close();
    }
}
```

## OUTPUT:
<img width="1221" height="849" alt="image" src="https://github.com/user-attachments/assets/731c3db5-21a6-4ad0-b87a-7d8229274e4d" />

## RESULT:
The program ensures all services use a single Logger instance, records each log entry, and displays the complete log history after every new entry.
