import java.util.*;



public class Quad {


    public static void main(String[] args) {

        Scanner keyboard = new Scanner(System.in);


        int a, b, c;
        double root1, root2, first;


        System.out.println("Enter a");
        a = keyboard.nextInt();

        System.out.println("Enter b");
        b = keyboard.nextInt();

        System.out.println("Enter c");
        c = keyboard.nextInt();


        System.out.println("Your quadratic equation will be " + a + "x^2" + "+" + b + "x" + "+" + c);


        first = (b * b) - (4 * a * c);       //Handling the first case. If whats under the square root is greater than 0 then the roots are real and unequal
        if (first > 0) {

            root1 = (-b + Math.sqrt(first)) / (2 * a);
            root2 = (-b - Math.sqrt(first)) / (2 * a);
            System.out.println("First root is: " + root1);
            System.out.println("Second root is: " + root2);

        } else if (first == 0) {
            System.out.println("Roots are real and equal");    //Handling the case if whats under the square root is equal to 0

            root1 = (-b + Math.sqrt(first)) / (2 * a);              //If this equals 0 then you will only have one root based on the rules of quadratic formula
            System.out.println("The only root is " + root1);
        } else {
            System.out.println("Roots are non existent");
        }

    }
}


/*
package edu.cau.cs301;


 This is an abstract class for CIS301 Project 1


public abstract class AbstractQuadraticEquationSolver {


    /**
     * parses the equation and addresses all possible cases.

    public abstract void parseEquation();
    /**
     * solves the root of the quadratic equation

    public abstract void solve();


     * generates the readme usage/help for the quadratic equation.
     * @return returns the help/usage

    public abstract String readMe();
}*/
