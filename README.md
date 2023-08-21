# C-Program-for-finding-the-occurrence-of-a-digit-in-a-given-number

Occurrence of a Digit in a given Number in C
Here, in this page we will discuss the program to find the occurrence of a digit in a given number in C .The input may lie within the range of integer.
 
If the digit does not occur in the input it should print 0 else the count of digits.
 
 
Example :
Input : Enter a number : 897982
             Enter the digit : 9
Output :  2
Explanation : The digit 9 occurs twice
Algorithm
Declare variable count that will count the required number of occurrences
Take a while loop.
Declare a variable rem to store every digit of the number to be compared.
Compare rem with the digit
if rem equals digit increment count.
n=n/10
Print the value of count.
We will implements the above algorithm using two methods,

Method 1 : Iterative way
Method 2 : Recursive way.
Method 1 : Code in C
Run
//Write a program to print the Occurrence of a Digit in a given Number in C
#include<stdio.h>

int main() {

    int n = 890190798; 
    int d = 9; 

    int count=0; 

    while(n) {

        int rem = n%10; 
        if(rem == d){
            count++;
        }
        n=n/10; 
    }

    printf("%d",count);

    return 0;

}

Output:
3
Related Pages
Convert digit/number to words

Counting number of days in a given month of a year
 
Finding number of integers which has exactly x divisors

Finding Roots of a quadratic equation

Power of a Number 

Method 2 : Code in C
Run
//Write a program to print the Occurrence of a Digit in a given Number in C
#include <stdio.h>

int count(int n, int d){
    if(n<=0)
    return 0;
    
    int rem = n%10;
    
    if(rem == d){
        return 1 + count(n/10, d);
    }
    
    return count(n/10, d);
}
int main() {

    int n = 890190798; 
    int d = 9; 
    
    int x = count(n, d);
    printf("%d",x);

    return 0;

}

Output:
3
