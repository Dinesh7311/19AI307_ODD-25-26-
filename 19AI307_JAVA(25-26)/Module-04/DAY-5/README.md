# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Write a small Java MVC program to track a Bank Account balance. Controller can deposit and withdraw, and the view should show the updated balance.

## AIM:
To implement a simple Java Program using the MVC (Model–View–Controller) Pattern to manage a Bank Account.

## ALGORITHM :
1.Read initial balance.

2.Create Model (BankAccount), View, and Controller objects.

3.Read number of operations.

4.For each operation:

     .If "deposit" → controller.deposit(amount)

     .If "withdraw" → controller.withdraw(amount)

5.Controller updates Model and calls View to display balance or error.

6.End.





## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by:DINESH S
RegisterNumber:212224240038 
*/
```

## SOURCE CODE:
```
import java.util.*;

public class BankMVCSkeleton {

    static class BankAccount {
        private double balance;

        public BankAccount(double balance) {
            this.balance = balance;
        }

        public void deposit(double amount) {
            balance += amount;
        }

        public boolean withdraw(double amount) {
            if (amount <= balance) {
                balance -= amount;
                return true;
            }
            return false;
        }

        public double getBalance() {
            return balance;
        }
    }

    static class AccountView {
        public void showBalance(double balance) {
            System.out.printf("Current Balance: \u20B9%.2f%n", balance);
        }

        public void showError(String message) {
            System.out.println(message);
        }
    }

    static class AccountController {
        private BankAccount model;
        private AccountView view;

        public AccountController(BankAccount model, AccountView view) {
            this.model = model;
            this.view = view;
        }

        public void deposit(double amount) {
            model.deposit(amount);
            view.showBalance(model.getBalance());
        }

        public void withdraw(double amount) {
            if (model.withdraw(amount)) {
                view.showBalance(model.getBalance());
            } else {
                view.showError("Withdrawal failed: insufficient balance.");
            }
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        double initialBalance = sc.nextDouble();
        BankAccount model = new BankAccount(initialBalance);
        AccountView view = new AccountView();
        AccountController controller = new AccountController(model, view);

        int operations = sc.nextInt();
        for (int i = 0; i < operations; i++) {
            String op = sc.next();
            double amount = sc.nextDouble();
            if (op.equalsIgnoreCase("deposit")) {
                controller.deposit(amount);
            } else if (op.equalsIgnoreCase("withdraw")) {
                controller.withdraw(amount);
            }
        }

        sc.close();
    }
}
```

## OUTPUT:
<img width="1251" height="792" alt="image" src="https://github.com/user-attachments/assets/1ff72479-a180-4a39-82b9-26689f2b0b49" />

## RESULT:
The program updates the balance after each deposit or valid withdrawal and displays the current balance. Invalid withdrawals show an error.
