# Permutations-in-which-n-people-can-occupy-r-seats-in-a-classroom-in-java

Which n people can occupy r seats in a classroom in Java
Our Aim is to write a Java code to find all the possible permutations in which (n) people can occupy (r) number of seats in a classroom.

Suppose (n) number  students are looking to find (r) seats in a classroom so how will they do it . They will do it with simple formula which is given by 

                                                                n P r  =    n! / (n-r)!
Permutation
Way 2 Of Asking Question
Write code to find all possible permutations in which n people can occupy r seats in a theater
Problem Statement :
In a classroom some of the seats are already occupied by students and only a few seats are available in the classroom. The available seats are assumed as r and n number of students are looking for the seat. We need to find in how many different permutations n number of students can sit on r number of chairs.

Algorithm
Input number of students in n
Input number of seats in r
Use permutation formula { factorial(n) / factorial(n-r) }
Print Output
Permutations in Java
Related Pages
Octal to Binary conversion

Quadrants in which a given coordinate lies
 
Maximum number of handshakes

Addition of two fractions

Replace all 0’s with 1 in a given integer

Java code
Run
import java.util.*;  
import java.io.*;

public class Main
    {  
      public static void main(String[] args)  
        {  

            int n, r, per, fact1, fact2;  

            Scanner sc =  new Scanner(System.in);  

            System.out.println("Enter the Value of n: ");  
            n = sc.nextInt();

            System.out.println("Enter the Value of r: ");
            r = sc.nextInt();  

            fact1 = 1;  

            for (int i = n; i > 1; i=i-1)  
            {  
                fact1 = fact1 * i;  //calculating factorial (n!)
            }  

            int number;  

            number = n - r;  

            fact2 = 1;  

            for (int i = number; i > 1; i=i-1)  
            {  
                fact2 = fact2 * i;  //calculating factorial ((n-r)!)
            }  

            per = fact1 / fact2;  //calculating  nPr

            System.out.println(per+" ways");  
    }  
}
Output
Enter number of people: 5
Enter number of seats: 9
Total possible arrangements: 120
