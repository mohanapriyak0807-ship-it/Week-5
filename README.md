# Week-5

import java.util.ArrayList;
import java.util.Scanner;

class Week5 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String[] products = {
            "Running Shoes",
            "Sports Shoes",
            "Leather Belt",
            "Sports Cap"
        };

        ArrayList<String> cart = new ArrayList<>();

        System.out.println("Available Products:");

        for (int i = 0; i < products.length; i++) {
            System.out.println((i + 1) + ". " + products[i]);
        }

        System.out.print("Enter product number to add to cart: ");
        int choice = sc.nextInt();

        if (choice >= 1 && choice <= products.length) {
            cart.add(products[choice - 1]);
            System.out.println(products[choice - 1] + " added to cart!");
        } else {
            System.out.println("Invalid product number!");
        }

        System.out.println("Your Cart: " + cart);

        sc.close();
    }
}
