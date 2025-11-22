# Ex.No:3(C) ABSTRACTION

## QUESTION:
A group of researchers receives mysterious numerical sequences believed to be sent by intelligent alien life. To decode them, scientists have built intelligent SignalAgents that follow abstract processing rules. Each agent listens to the numbers differently.

## AIM:
To build SignalAgents that decode mysterious numerical sequences using different processing rules.

## ALGORITHM :
1.Read signal array and agent type

2.If type = 1 → use PrimeAgent to sum prime numbers

3.Else → use MirrorAgent to check symmetry

4.Print the result

5.End

## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by:DINESH S 
RegisterNumber:212224240038
*/
```

## SOURCE CODE:
```
import java.util.*;

abstract class SignalAgent {
    abstract int decodeSignal(int[] signal);
}

class PrimeAgent extends SignalAgent {
    private boolean isPrime(int n) {
        if (n < 2) return false;
        for (int i = 2; i * i <= n; i++) {
            if (n % i == 0) return false;
        }
        return true;
    }

    int decodeSignal(int[] signal) {
        int sum = 0;
        for (int num : signal) {
            if (isPrime(num)) sum += num;
        }
        return sum;
    }
}

class MirrorAgent extends SignalAgent {
    int decodeSignal(int[] signal) {
        int n = signal.length;
        for (int i = 0; i < n / 2; i++) {
            if (signal[i] != signal[n - i - 1]) return -1;
        }
        return 1;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] signal = new int[n];
        for (int i = 0; i < n; i++) signal[i] = sc.nextInt();
        int type = sc.nextInt();
        SignalAgent agent;
        if (type == 1) {
            agent = new PrimeAgent();
            System.out.println(agent.decodeSignal(signal));
        } else {
            agent = new MirrorAgent();
            int result = agent.decodeSignal(signal);
            System.out.println(result == 1 ? "BALANCED" : "BROKEN");
        }
        sc.close();
    }
}
```






## OUTPUT:

<img width="520" height="430" alt="image" src="https://github.com/user-attachments/assets/989725f5-eee3-4f21-a545-05de99d02030" />

## RESULT:
The program decodes the signal by either summing prime numbers or checking if the sequence is symmetric, then prints the final outcome.
