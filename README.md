import java.util.Scanner;

class MobilePhone {
    // Attributes
    String brand;
    String model;
    double price;

    // Method to display phone details
    void displayDetails() {
        System.out.println("Brand: " + brand);
        System.out.println("Model: " + model);
        System.out.println("Price: $" + price);
    }

    // Method to simulate making a call
    void makeCall(String number) {
        System.out.println("Calling " + number + " from " + brand + " " + model);
    }

    // Method to simulate sending a message
    void sendMessage(String number, String message) {
        System.out.println("Sending '" + message + "' to " + number);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Create first phone
        MobilePhone phone1 = new MobilePhone();
        System.out.println("Enter details for Phone 1:");
        System.out.print("Brand: ");
        phone1.brand = scanner.nextLine();
        System.out.print("Model: ");
        phone1.model = scanner.nextLine();
        System.out.print("Price: ");
        phone1.price = scanner.nextDouble();
        scanner.nextLine(); // consume newline

        // Create second phone
        MobilePhone phone2 = new MobilePhone();
        System.out.println("\nEnter details for Phone 2:");
        System.out.print("Brand: ");
        phone2.brand = scanner.nextLine();
        System.out.print("Model: ");
        phone2.model = scanner.nextLine();
        System.out.print("Price: ");
        phone2.price = scanner.nextDouble();
        scanner.nextLine(); // consume newline

        // Display details
        System.out.println("\nDetails of Phone 1:");
        phone1.displayDetails();

        System.out.println("\nDetails of Phone 2:");
        phone2.displayDetails();

        // Make a call and send a message from phone1
        System.out.print("\nPhone 1 - Enter number to call: ");
        String number1 = scanner.nextLine();
        phone1.makeCall(number1);

        System.out.print("Phone 1 - Enter number to message: ");
        String msgNumber1 = scanner.nextLine();
        System.out.print("Phone 1 - Enter message: ");
        String message1 = scanner.nextLine();
        phone1.sendMessage(msgNumber1, message1);

        // Make a call and send a message from phone2
        System.out.print("\nPhone 2 - Enter number to call: ");
        String number2 = scanner.nextLine();
        phone2.makeCall(number2);

        System.out.print("Phone 2 - Enter number to message: ");
        String msgNumber2 = scanner.nextLine();
        System.out.print("Phone 2 - Enter message: ");
        String message2 = scanner.nextLine();
        phone2.sendMessage(msgNumber2, message2);

        scanner.close();
    }
}
