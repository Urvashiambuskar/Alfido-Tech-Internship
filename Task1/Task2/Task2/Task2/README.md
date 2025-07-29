# ✅ Task 2 – Calculator Program

Java console-based calculator for basic arithmetic operations.


## 🎯 Objective

Create a Java program to perform:
- Addition
- Subtraction
- Multiplication
- Division

User inputs two numbers and selects the desired operation.


## 💻 Java Code

import java.util.Scanner;

public class Calculator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.println("Enter first number:");
        double num1 = sc.nextDouble();

        System.out.println("Enter second number:");
        double num2 = sc.nextDouble();

        System.out.println("Choose operation (+, -, *, /):");
        char operator = sc.next().charAt(0);

        double result;

        switch (operator) {
            case '+':
                result = num1 + num2;
                break;

            case '-':
                result = num1 - num2;
                break;

            case '*':
                result = num1 * num2;
                break;

            case '/':
                if (num2 != 0)
                    result = num1 / num2;
                else {
                    System.out.println("Cannot divide by zero!");
                    return;
                }
                break;

            default:
                System.out.println("Invalid operator!");
                return;
        }

        System.out.println("Result: " + result);
    }
}

#OUTPUT:
Enter first number: 5  
Enter second number: 5
Choose operation: +  
Result: 10.0

