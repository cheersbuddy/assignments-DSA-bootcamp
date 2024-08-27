```
import java.util.*;
class HelloWorld {
    public static void main(String[] args) {
        double x= 100;
        double y=x*0.012;
        System.out.println(" INR is " + x);
        System.out.println(" USD is " + y );
    }
}
```

```
 INR is 100.0
 USD is 1.2
```
---
# REFER
```
import java.util.Scanner;

public class CurrencyConverter {
    public static void main(String[] args) {
        // Create a Scanner object for user input
        Scanner scanner = new Scanner(System.in);
        // Display a welcome message
        System.out.println("Welcome to the Currency Converter!");
        // Main program loop
        while (true) {
            // Display the menu
            System.out.println("\nMenu:");
            System.out.println("1. Convert USD to EUR");
            System.out.println("2. Convert EUR to USD");
            System.out.println("3. Quit");
            System.out.print("Enter your choice: ");
            // Read the user's choice
            int choice = scanner.nextInt();
            // Perform the chosen operation
            switch (choice) {
                case 1:
                    convertUSDToEUR(scanner);
                    break;
                case 2:
                    convertEURToUSD(scanner);
                    break;
                case 3:
                    System.out.println("Thank you for using the Currency Converter!");
                    // Close the scanner
                    scanner.close();
                    return;
                default:
                    System.out.println("Invalid choice. Please try again.");
            }
        }
    }

    // Conversion rates (hardcoded for simplicity)
    private static double usdToEurRate = 0.85;
    private static double eurToUsdRate = 1.18;

    // Method to convert USD to EUR
    private static void convertUSDToEUR(Scanner scanner) {   // here ' Scanner scanner' means passing the Scanner class and scanner class name as argument instead of writing  Scanner scanner = new Scanner(System.in);  in every class.
        System.out.print("Enter the amount in USD: ");
        double usdAmount = scanner.nextDouble();
        double eurAmount = usdAmount * usdToEurRate;
        System.out.println(usdAmount + " USD is equivalent to " + eurAmount + " EUR");
    }

    // Method to convert EUR to USD
    private static void convertEURToUSD(Scanner scanner) {
        System.out.print("Enter the amount in EUR: ");
        double eurAmount = scanner.nextDouble();
        double usdAmount = eurAmount * eurToUsdRate;
        System.out.println(eurAmount + " EUR is equivalent to " + usdAmount + " USD");
    }
}

```
```
Welcome to the Currency Converter!
Menu:
1. Convert USD to EUR
2. Convert EUR to USD
3. Quit
Enter your choice: 1
Enter the amount in USD: 100
100.0 USD is equivalent to 85.0 EUR
Menu:11
1. Convert USD to EUR
2. Convert EUR to USD
3. Quit
Enter your choice: 2
Enter the amount in EUR: 50
50.0 EUR is equivalent to 59.0 USD
Menu:
1. Convert USD to EUR
2. Convert EUR to USD
3. Quit
Enter your choice: 3
Thank you for using the Currency Converter!
```
