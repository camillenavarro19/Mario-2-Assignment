package com.company;

import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        //write your code here
        int height;
        Scanner mario = new Scanner(System.in);
        do {
            System.out.println("How tall is your tower? Enter a # between 1-8: ");
            while (!mario.hasNextInt()) {
                mario.next();
            }
            height = mario.nextInt();
            if ((height < 1)) {
                System.out.println("Invalid input, please try again ");
            }
            if ((height > 8)) {
                System.out.println("Invalid input, please try again ");
            }
        }
        while (height < 1 || height > 8);
        System.out.println("Height: " + height);
        System.out.println("Stored height: " + height);

        for (int row = 0; row < height; row++) {
            for (int column = 1; column < height - row; column++) {
                System.out.print(".");
            }
            for (int hash = 0; hash <= row; hash++) {
                System.out.print("#");
            }
            System.out.println("");
            }
        }
    }
