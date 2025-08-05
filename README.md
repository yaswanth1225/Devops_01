public class FibonacciSeries {

    public static void main(String[] args) {
        int n = 50; // Number of Fibonacci numbers to generate

        // Handle base cases
        if (n <= 0) {
            System.out.println("Please enter a positive integer for n.");
            return;
        } else if (n == 1) {
            System.out.println("Fibonacci Series up to " + n + " terms:");
            System.out.println("0");
            return;
        }

        // Initialize first two Fibonacci numbers
        long fib1 = 0;
        long fib2 = 1;

        System.out.println("Fibonacci Series up to " + n + " terms:");

        // Print the first two numbers
        System.out.print(fib1 + ", " + fib2);

        // Generate and print the remaining Fibonacci numbers
        for (int i = 2; i < n; i++) {
            long nextFib = fib1 + fib2;
            System.out.print(", " + nextFib);
            fib1 = fib2;
            fib2 = nextFib;
        }
        System.out.println(); // Newline at the end
    }
}
