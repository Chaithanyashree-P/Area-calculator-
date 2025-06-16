import java.util.Scanner;
public class AreaCalculator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Area Calculator");
        System.out.println("1. Square");
        System.out.println("2. Rectangle");
        System.out.println("3. Circle");
        System.out.print("Choose an option: ");
        int option = scanner.nextInt();

        switch (option) {
            case 1:
                     System.out.print("Enter side length of square: ");
                double side = scanner.nextDouble();
                System.out.println("Area of square: " + calculateSquareArea(side));
                break;
            case 2:
                System.out.print("Enter length of rectangle: ");
                double length = scanner.nextDouble();
                System.out.print("Enter width of rectangle: ");
                double width = scanner.nextDouble();
                System.out.println("Area of rectangle: " + calculateRectangleArea(length, width));
                break;
            case 3:
                System.out.print("Enter radius of circle: ");
                double radius = scanner.nextDouble();
                System.out.println("Area of circle: " + calculateCircleArea(radius));
                break;
            default:
                System.out.println("Invalid option");
        }
    }

    private static double calculateSquareArea(double side) {
        return side * side;
    }

    private static double calculateRectangleArea(double length, double width) {
        return length * width;
    }

    private static double calculateCircleArea(double radius) {
        return Math.PI * radius * radius;
    }
}
