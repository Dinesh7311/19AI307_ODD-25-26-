# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
Welcome to MatchIt – a dating app that automatically notifies users when their preferred type of match joins the platform.

## AIM:
To develop a system that automatically alerts users when new members who match their preferred criteria join the MatchIt dating platform.

## ALGORITHM :
1.Register users with their preferences

2.For each new signup, check which users prefer that type

3.Notify matching users

4.End

## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by:DINESH S 
RegisterNumber:212224240038 
*/
```

## SOURCE CODE:
```
import java.util.*;

interface Observer {
    void notify(String name, String type);
    String getPreference();
}

class User implements Observer {
    private String name;
    private String preference;

    public User(String name, String preference) {
        this.name = name;
        this.preference = preference;
    }

    @Override
    public void notify(String newUserName, String type) {
        System.out.println(name + ": Omg! A new " + type + "? MatchIt, you know me too well! (It’s " + newUserName + "!)");
    }

    @Override
    public String getPreference() {
        return preference;
    }
}

class MatchItServer {
    private List<Observer> users = new ArrayList<>();

    public void register(Observer user) {
        users.add(user);
    }

    public void newSignup(String name, String type) {
        System.out.println("New User Joined: " + name + " - Type: " + type);
        for (Observer user : users) {
            if (user.getPreference().equalsIgnoreCase(type)) {
                user.notify(name, type);
            }
        }
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        MatchItServer server = new MatchItServer();

        int n = sc.nextInt();
        sc.nextLine();
        for (int i = 0; i < n; i++) {
            String[] userInfo = sc.nextLine().split(" ");
            server.register(new User(userInfo[0], userInfo[1]));
        }

        int m = sc.nextInt();
        sc.nextLine();
        for (int i = 0; i < m; i++) {
            String[] newUser = sc.nextLine().split(" ");
            server.newSignup(newUser[0], newUser[1]);
        }
        sc.close();
    }
}
```

## OUTPUT:
<img width="1278" height="589" alt="image" src="https://github.com/user-attachments/assets/fba603f2-beca-4c91-9a79-f555747807ce" />

## RESULT:
The program registers users with preferences and notifies them whenever a new signup matches their preferred type.

