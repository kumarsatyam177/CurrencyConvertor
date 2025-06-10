import java.util.Scanner;

public class CurrencyConverter {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.println("WELCOME TO CURRENCY CONVERTER!");
        System.out.println("1. USD TO RUPEE");
        System.out.println("2. RUPEE TO USD");
        System.out.println("3. EURO TO RUPEE");
        System.out.println("4. RUPEE TO EURO");

        System.out.print("ENTER YOUR CHOICE (1 OR 2 OR 3 OR 4): ");
        int choice = sc.nextInt();

        switch (choice) {
            case 1:
                System.out.print("ENTER THE AMOUNT IN USD: ");
                double usd = sc.nextDouble();
                double rupeeFromUsd = usdToRupee(usd);
                System.out.println("CONVERTED AMOUNT IN RUPEE: " + rupeeFromUsd);
                break;

            case 2:
                System.out.print("ENTER THE AMOUNT IN RUPEE: ");
                double rupee1 = sc.nextDouble();
                double usdFromRupee = rupeeToUsd(rupee1);
                System.out.println("CONVERTED AMOUNT IN USD: " + usdFromRupee);
                break;

            case 3:
                System.out.print("ENTER THE AMOUNT IN EURO: ");
                double euro = sc.nextDouble();
                double rupeeFromEuro = euroToRupee(euro);
                System.out.println("CONVERTED AMOUNT IN RUPEE: " + rupeeFromEuro);
                break;

            case 4:
                System.out.print("ENTER THE AMOUNT IN RUPEE: ");
                double rupee2 = sc.nextDouble();
                double euroFromRupee = rupeeToEuro(rupee2);
                System.out.println("CONVERTED AMOUNT IN EURO: " + euroFromRupee);
                break;

            default:
                System.out.println("INVALID CHOICE. PLEASE SELECT 1 OR 2 OR 3 OR 4.");
        }

        sc.close();
    }

    public static double usdToRupee(double usd) {
        return usd * 85.79; // As of 08/06/25
    }

    public static double rupeeToUsd(double rupee) {
        return rupee * 0.012; // As of 08/06/25
    }

    public static double euroToRupee(double euro) {
        return euro * 97.80; // As of 08/06/25
    }

    public static double rupeeToEuro(double rupee) {
        return rupee * 0.010; // As of 08/06/25
    }
}
