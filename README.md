# Write-a-Program-to-Convert-Binary-Number-To-Decimal-Number-in-Java.
Write a Program to Convert Binary Number To Decimal Number in Java. Write a Program to find Decimal Equivalent of a number.


Java-How-To-Program-9th-Ed.-Deitel-
Java Program to find Gas Mileage

Write a Program to Convert Binary Number To Decimal Number in Java.

4.31 (Printing the Decimal Equivalent of a Binary Number) Write an application that inputs an
integer containing only 0s and 1s (i.e., a binary integer) and prints its decimal equivalent. 

[Hint: Use the remainder and division operators to pick off the binary number’s digits one at a time, from right
to left. In the decimal number system, the rightmost digit has a positional value of 1 and the next
digit to the left a positional value of 10, then 100, then 1000, and so on. The decimal number 234
can be interpreted as 4 * 1 + 3 * 10 + 2 * 100. In the binary number system, the rightmost digit has
a positional value of 1, the next digit to the left a positional value of 2, then 4, then 8, and so on.
The decimal equivalent of binary 1101 is 1 * 1 + 0 * 2 + 1 * 4 + 1 * 8, or 1 + 0 + 4 + 8 or, 13.]


            import java.util.Scanner;

            public class Main {



                public static void main(String[] args) {


                    Scanner console = new Scanner(System.in);

                    System.out.println("Enter a Binary Number Such that 1101: ");

                    int BinaryNumber = console.nextInt();

                    int r, DecimalNumber=0, power = 0;

                    int temp=BinaryNumber;

                    while (BinaryNumber>0){

                         r = BinaryNumber%10;

                         DecimalNumber= DecimalNumber+(r*(int)(Math.pow(2,power)));

                         BinaryNumber=BinaryNumber/10;

                         power++;
                    }
                    System.out.println("Decimal Equivalent of a Number "+ temp +"is: "+DecimalNumber );
                }
            }
