# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for set the priority and name of the current thread.Consider two threads t1 and t2


## AIM:
To create and demonstrate threads in Java by assigning names and priorities, and to display their details.

## ALGORITHM :
1.Start

2.Create a Scanner object to read input.

3.Read two thread names from the user.

4.Create two Thread objects (t1 and t2).

5.Set the names of the threads using setName().

6.Set the priorities of the threads using setPriority() (e.g., t1 = 4, t2 = 2).

7.Print the thread details using System.out.println().

8.Close the scanner.

9.End





## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: DINESH S
RegisterNumber: 212224240038 
*/
```

## SOURCE CODE:
```

import java.util.Scanner;

public class ThreadPriorityExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String name1 = sc.nextLine();
        String name2 = sc.nextLine();

        Thread t1 = new Thread();
        Thread t2 = new Thread();

        t1.setName(name1);
        t1.setPriority(4);

        t2.setName(name2);
        t2.setPriority(2);

        System.out.println(t1);
        System.out.println(t2);

        sc.close();
    }
}
```

## OUTPUT:
<img width="1327" height="419" alt="image" src="https://github.com/user-attachments/assets/1215a512-615e-49bc-b9b9-8036fc61ba33" />

## RESULT:
The program creates two threads with user-specified names, assigns them different priorities, and prints their details showing the name, priority, and thread group.
