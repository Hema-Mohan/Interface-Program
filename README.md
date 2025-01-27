# Interface-Program
import java.util.Scanner;
// Define the Calculator interface
interface Calculator {
double add(double a, double b);
double subtract(double a, double b);
double multiply(double a, double b);
double divide(double a, double b);
}
// Implement the interface in SimpleCalculator
 class SimpleCalculator implements Calculator{
    @Override
    public double add(double a,double b){
        return a+b;
    }
    @Override
    public double subtract(double a,double b){
        return a-b;
    }
    @Override
    public double multiply(double a,double b){
        return a*b;
    }
    @Override
    public double divide(double a, double b) {
    if (b == 0) {
    System.out.println("Error: Division by zero is not allowed!");
    return Double.NaN; // Return &quot;Not a Number&quot; if division by zero
    }
    return a/b;
    }
 }
// Main class to test the program
public class CalculatorProgram {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Calculator calculator = new SimpleCalculator();
        System.out.println("Welcome to Simple Calculator!");
        // Input two numbers
        System.out.print("Enter the first no:");
        double num1= sc.nextDouble();
        System.out.print("Enter the second no:");
        double num2= sc.nextDouble();
        // Perform calculations
        System.out.println("\n RESULTS\n");
        System.out.println("Addition:" + calculator.add(num1, num2));
        System.out.println("Subtraction:" + calculator.subtract(num1, num2));
        System.out.println("Multiplication:" + calculator.multiply(num1, num2));
        System.out.println("Division:" + calculator.divide(num1, num2));
    }    
}

OUTPUT:

Welcome to Simple Calculator!
Enter the first no:10
Enter the second no:2

 RESULTS

Addition:12.0
Subtraction:8.0
Multiplication:20.0
Division:5.0
