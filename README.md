import java.util.Scanner;
public class SimpleCarRental {
    static class Car {
        String id;
        String brand;
        boolean available;
        Car(String id, String brand) {
            this.id = id;
            this.brand = brand;
            this.available = true; 
        }
        void rent() {
            if (available) {
                available = false;
                System.out.println(brand + " has been rented.");
            } else {
                System.out.println(brand + " is already rented.");
            }
        }
        void giveBack() {
            available = true;
            System.out.println(brand + " has been returned.");
        }
        void showCar() {
            System.out.println(id + " - " + brand + " | Available: " + available);
        }
    }
    public static void main(String[] args) {
        Car car1 = new Car("C001", "Toyota");
        Car car2 = new Car("C002", "Honda");

        System.out.println("Cars in the system:");
        car1.showCar();
        car2.showCar();

       
        car1.rent();

        
        car1.rent();

       
        car1.giveBack();

       
        System.out.println("Updated car list:");
        car1.showCar();
        car2.showCar();
    }
}
