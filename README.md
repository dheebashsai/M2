# EX-06 - Looping
## AIM:
Write a C program to print even numbers ranging from M to N (including M and N values).

## ALGORITHM:
1.	Declare two integer variables to store the values of M and N.
2.	Use the printf function to prompt the user to enter the values of M and N.
3.	Use the scanf function to read the values of M and N from the user.
4.	Use a loop (for or while) to iterate from M to N.
5.	Inside the loop, check if the current number is even.
6.	If the current number is even, print it.
7.	Continue the loop until you have iterated through all numbers from M to N.

## PROGRAM:
    #include <stdio.h>
    
    int main() {
        int M, N;
    
        // Step 2: Prompt user
        printf("Enter the values of M and N: ");
        
        // Step 3: Read values
        scanf("%d %d", &M, &N);
    
        printf("Even numbers from %d to %d are:\n", M, N);
    
        // Step 4: Loop from M to N
        for (int i = M; i <= N; i++) {
            // Step 5: Check if even
            if (i % 2 == 0) {
                // Step 6: Print even number
                printf("%d ", i);
            }
        }
    
        printf("\n");
    
        return 0;
    }


## OUTPUT:
Enter the values of M and N: 3 15
Even numbers from 3 to 15 are:
4 6 8 10 12 14 







## RESULT:
Thus the program to print even numbers ranging from M to N (including M and N values) has been executed successfully
 
 


# EX-07-Nested-loop

## AIM:

Write a C program to print the given triangular pattern using loop.

## ALGORITHM:

1.	Declare a variable to store the number of rows in the triangle.
2.	Use the printf function to prompt the user to enter the number of rows.
3.	Use a loop (for or while) to iterate through each row.
4.	Inside the loop, use another loop to print the desired number of asterisks for each row.
5.	Continue the loop until you have printed the entire triangular pattern.

## PROGRAM:
    #include <stdio.h>
    
    int main() {
        int rows;
    
        // Step 2: Prompt user for number of rows
        printf("Enter the number of rows: ");
        scanf("%d", &rows);
    
        // Step 3: Loop through each row
        for (int i = 1; i <= rows; i++) {
            // Step 4: Print i asterisks for the current row
            for (int j = 1; j <= i; j++) {
                printf("* ");
            }
            printf("\n");  // Move to the next line after each row
        }
    
        return 0;
    }



## OUTPUT:
        Enter the number of rows: 5
        * 
        * * 
        * * * 
        * * * * 
        * * * * * 





## RESULT:

Thus the program to print the given triangular pattern using loop has been executed successfully
 
 


# EX-08-Functions

## AIM:

Write a C program to perform addition and subtraction of two numbers using functions (with argument and without return type).

## ALGORITHM:

1.	Declare two functions, one for addition and one for subtraction. Both functions should take two integer arguments.
2.	Inside the addition & subtraction function, add & subtract the two numbers and print the result.
3.	In the main function, declare two integer variables and read their values from the user.
4.	Call the addition and subtraction functions, passing the two numbers as arguments.

## PROGRAM:
    #include <stdio.h>
    
    // Step 1: Declare addition function
    void addition(int a, int b) {
        int sum = a + b;
        printf("Addition: %d + %d = %d\n", a, b, sum);
    }
    
    // Step 1: Declare subtraction function
    void subtraction(int a, int b) {
        int diff = a - b;
        printf("Subtraction: %d - %d = %d\n", a, b, diff);
    }
    
    int main() {
        int num1, num2;
    
        // Step 3: Read two numbers from the user
        printf("Enter two numbers: ");
        scanf("%d %d", &num1, &num2);
    
        // Step 4: Call the functions
        addition(num1, num2);
        subtraction(num1, num2);
    
        return 0;
    }


## OUTPUT:
Enter two numbers: 10 5
Addition: 10 + 5 = 15
Subtraction: 10 - 5 = 5






## RESULT:

Thus the program to perform addition and subtraction of two numbers using functions has been executed successfully
 
 


# EX-09-Use For Loop

## AIM:

Write a c program to find the sum of odd digits using for loop

## ALGORITHM:

1.	Declare variables to store the input number and the sum of odd digits.
2.	Initialize the sum of odd digits to 0.
3.	Use a for loop to iterate through each digit of the input number.
4.	Inside the loop, extract the rightmost digit of the number (using the modulo operator % and division by 10).
5.	If the digit is odd, add it to the sum of odd digits.
6.	Print the sum of odd digits.

## PROGRAM:
    #include <stdio.h>
    
    int main() {
        int number, sum = 0, digit;
        int temp;
    
        // Step 1 & 2: Input and initialize sum
        printf("Enter a number: ");
        scanf("%d", &number);
    
        // Use temp to preserve original number since we need to iterate through digits
        temp = number;
    
        // Step 3: Iterate through each digit using a for loop
        for (; temp > 0; temp = temp / 10) {
            // Step 4: Extract rightmost digit
            digit = temp % 10;
    
            // Step 5: Check if digit is odd
            if (digit % 2 != 0) {
                sum += digit;
            }
        }
    
        // Step 6: Print the sum of odd digits
        printf("Sum of odd digits in %d is: %d\n", number, sum);
    
        return 0;
    }


## OUTPUT:

Enter a number: 123456
Sum of odd digits in 123456 is: 9



## RESULT:

Thus the program to find the sum of odd digits using for loop has been executed successfully.




# EX – 10 - Factorial of a Number Using a Function
## AIM:
To write a C program that calculates the factorial of a given number using a user-defined function.
## ALGORITHM:
1.	Start
2.	Declare the function fact().
3.	In the main() function, call the fact() function.
4.	In fact() function:
a.	Declare variables i, N, and fact (initialized to 1).
b.	Read an integer N from the user.
c.	Use a for loop from 1 to N:
i.	Multiply fact by i in each iteration.
d.	After the loop, print the factorial value.
5.	End

## PROGRAM:
    #include <stdio.h>
    
    // Step 2: Declare the function fact()
    void fact() {
        int i, N;
        unsigned long long fact = 1; // Use unsigned long long to handle large factorials
    
        // Step 4b: Read an integer N from user
        printf("Enter a number to find its factorial: ");
        scanf("%d", &N);
    
        // Handle negative numbers
        if (N < 0) {
            printf("Factorial of negative numbers is not defined.\n");
            return;
        }
    
        // Step 4c: Use for loop to calculate factorial
        for (i = 1; i <= N; i++) {
            fact *= i;
        }
    
        // Step 4d: Print factorial value
        printf("Factorial of %d is: %llu\n", N, fact);
    }
    
    int main() {
        // Step 3: Call fact() function
        fact();
        return 0;
    }


## OUTPUT:
Enter a number to find its factorial: 5
Factorial of 5 is: 120


## RESULT:
The program correctly computes the factorial of a given number using a separate function and displays the result.
 
