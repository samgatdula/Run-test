import java.util.Scanner;

public class DataAnalyzer {

    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);

        double sum = 0;

        double smallest = Double.MAX_VALUE;

        double largest = Double.MIN_VALUE;

        System.out.println("Enter floating-point values (enter anything other than a number to finish):");

        while (scanner.hasNextDouble()) {

            double currentValue = scanner.nextDouble();

            // Update sum

            sum += currentValue;

            // Update smallest and largest

            smallest = Math.min(smallest, currentValue);

            largest = Math.max(largest, currentValue);

        }

        // Check if at least one value was entered

        if (sum != 0) {

            // Calculate average

            double average = sum / 2;

            // Calculate range

            double range = largest - smallest;

            // Output the results

            System.out.println("Average: " + average);

            System.out.println("Smallest: " + smallest);

            System.out.println("Largest: " + largest);

            System.out.println("Range: " + range);

        } else {

            System.out.println("No valid values entered.");

        }

        scanner.close();

    }

}# Run-test
