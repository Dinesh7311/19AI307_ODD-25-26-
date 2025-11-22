# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
A food delivery application manages and processes food orders made by two categories of users: NormalUser and PrimeUser. Each food order contains basic information such as an order ID, the customer's name, the cost of the ordered items (referred to as the total amount), and the delivery charge applied to that order.

## AIM:
To develop a food delivery system that handles orders from NormalUser and PrimeUser, storing order details and applying appropriate delivery charges for each user type.

## ALGORITHM :
1.Start

2.Read user type, order ID, customer name, total amount, and delivery charge

3.If user type is Normal, calculate final amount = total + delivery charge

4.Else if user type is Prime, final amount = total + (delivery charge × 0.5)

5.Else use normal calculation

6.Display all order details

7.Repeat for next input

8.End
## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by:DINESH S
RegisterNumber:212224240038 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
import java.text.DecimalFormat;

class Order {
    String orderId;
    String customerName;
    double totalAmount;
    double deliveryCharge;

    public Order(String orderId, String customerName, double totalAmount, double deliveryCharge) {
        this.orderId = orderId;
        this.customerName = customerName;
        this.totalAmount = totalAmount;
        this.deliveryCharge = deliveryCharge;
    }

    double calculateFinalAmount() {
        return totalAmount + deliveryCharge;
    }

    void display(String userType) {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Order ID: " + orderId);
        System.out.println("Customer Name: " + customerName);
        System.out.println("User Type: " + userType);
        System.out.println("Total Amount: " + totalAmount);
        System.out.println("Delivery Charge: " + deliveryCharge);
        System.out.println("Final Amount: " + df.format(calculateFinalAmount()));
    }
}

class NormalUser extends Order {
    public NormalUser(String orderId, String customerName, double totalAmount, double deliveryCharge) {
        super(orderId, customerName, totalAmount, deliveryCharge);
    }

    @Override
    double calculateFinalAmount() {
        return totalAmount + deliveryCharge;
    }

    @Override
    void display(String userType) {
        super.display("Normal");
    }
}

class PrimeUser extends Order {
    public PrimeUser(String orderId, String customerName, double totalAmount, double deliveryCharge) {
        super(orderId, customerName, totalAmount, deliveryCharge);
    }

    @Override
    double calculateFinalAmount() {
        return totalAmount + (deliveryCharge * 0.5);
    }

    @Override
    void display(String userType) {
        super.display("Prime");
    }
}

public class FoodDeliveryApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        while (sc.hasNext()) {
            String type = sc.nextLine().trim();
            if (!sc.hasNext()) break;
            String orderId = sc.nextLine().trim();
            if (!sc.hasNext()) break;
            String name = sc.nextLine().trim();
            if (!sc.hasNextDouble()) break;
            double totalAmount = sc.nextDouble();
            if (!sc.hasNextDouble()) break;
            double deliveryCharge = sc.nextDouble();
            if (sc.hasNextLine()) sc.nextLine();

            Order order;
            if (type.equalsIgnoreCase("Normal")) {
                order = new NormalUser(orderId, name, totalAmount, deliveryCharge);
                order.display("Normal");
            } else if (type.equalsIgnoreCase("Prime")) {
                order = new PrimeUser(orderId, name, totalAmount, deliveryCharge);
                order.display("Prime");
            } else {
                order = new Order(orderId, name, totalAmount, deliveryCharge);
                order.display("General");
            }
        }

        sc.close();
    }
}
```
## OUTPUT:


<img width="960" height="762" alt="image" src="https://github.com/user-attachments/assets/f098d153-483e-4547-8da0-d1e1d12ba1b2" />


## RESULT:
The program reads order details, applies user-based delivery charges, calculates the final amount, and displays the order information.
