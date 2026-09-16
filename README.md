# 19AI304-Fundamentals-of-C-Programming-2025-Odd-M5
# IAPR-5- Module 5 - FoC
## 9. Implementation of recursion.
## 10. Implementation of programs using pointer arithmetic.
# Ex.No:21
  Implement a C program to demonstrate call by value and call by reference by swapping two integers using separate functions.
# Date : 10/9/26
# Aim:
 To implement a C program that illustrates the difference between call by value and call by reference by swapping two integer variables using two separate functions.
# Algorithm:
### Step 1:
  Start
### Step 2: 
  Include the standard input-output library: #include<stdio.h>.
### Step 3:
  Declare two functions:
  - `swapv(int, int)` for swapping using call by value  
  - `swapr(int *, int *)` for swapping using call by reference
### Step 4: 
  In the `main()` function, declare two integer variables `a` and `b` and initialize them with values (e.g., 10 and 20).
### Step 5: 
  Print the values of `a` and `b` before calling `swapv()`.
### Step 6: 
  Call the function `swapv(a, b)` and print the values of `a` and `b` after the function call to show that call by value does not change the original values.
### Step 7: 
  Print the values of `a` and `b` before calling `swapr()`.
### Step 8: 
  Call the function `swapr(&a, &b)` using the addresses of `a` and `b`.
### Step 9: 
  Print the values of `a` and `b` after the `swapr()` function call to show that call by reference successfully swaps the original values.
### Step 10: 
  Inside `swapv(x, y)` function:
  - **Step 10.1:** Swap the values of `x` and `y` using a temporary variable.  
  - **Step 10.2:** Print the swapped values (formal parameters).
### Step 11: 
  Inside `swapr(*x, *y)` function:
  - **Step 11.1:** Swap the values pointed to by `x` and `y`.  
  - **Step 11.2:** Print the swapped values (affects actual parameters).
### Step 12: 
  Stop
# Program:
```
#include <stdio.h>

// Step 3: Declare two functions
void swapv(int x, int y);
void swapr(int *x, int *y);

int main() {
    // Step 4: Declare two integer variables and initialize them
    int a = 10;
    int b = 20;
    
    // Step 5: Print before calling swapv()
    printf("Before call by value (swapv): a = %d, b = %d\n", a, b);
    
    // Step 6: Call swapv() and print after to show no change
    swapv(a, b);
    printf("After call by value (swapv) in main: a = %d, b = %d\n\n", a, b);
    
    // Step 7: Print before calling swapr()
    printf("Before call by reference (swapr): a = %d, b = %d\n", a, b);
    
    // Step 8 & 9: Call swapr() using addresses and print after to show change
    swapr(&a, &b);
    printf("After call by reference (swapr) in main: a = %d, b = %d\n", a, b);
    
    return 0;
}

// Step 10: Inside swapv(x, y) function
void swapv(int x, int y) {
    int temp;
    // Step 10.1: Swap using temporary variable
    temp = x;
    x = y;
    y = temp;
    // Step 10.2: Print swapped values
    printf("Inside swapv function: x = %d, y = %d\n", x, y);
}

// Step 11: Inside swapr(*x, *y) function
void swapr(int *x, int *y) {
    int temp;
    // Step 11.1: Swap the values pointed to by x and y
    temp = *x;
    *x = *y;
    *y = temp;
    // Step 11.2: Print swapped values
    printf("Inside swapr function: *x = %d, *y = %d\n", *x, *y);
}
```
# Output:
<img width="436" height="268" alt="image" src="https://github.com/user-attachments/assets/79106460-0779-489c-a28e-24917fa624b2" />

# Result: 
  Thus, the program was implemented and executed successfully, and the required output was obtained.


# 19AI304-Fundamentals-of-C-Programming-2025-Odd-M5
# IAPR-5- Module 5 - FoC
# Ex.No:22
  Implement a C program to generate the Fibonacci series using a recursive function. The program should accept a positive integer n and display the first n terms of the Fibonacci sequence.
# Date : 10/09/2026
# Aim:
  To implement a C program that uses a recursive function to generate and display the Fibonacci series for a given number of terms.
# Algorithm:
### Step 1:
  Start
### Step 2: 
  Include the standard input-output library: #include<stdio.h>.
### Step 3:
  Declare a recursive function `fibo(int x)` that returns the Fibonacci number at position `x`.  
### Step 4:
  In the `main()` function, declare variables `n` and `i`.  
### Step 5:
  Prompt the user to enter a positive integer `n`.  
### Step 6:
  Read the value of `n`.  
### Step 7:
  Display a message indicating that the Fibonacci series of `n` terms will be printed.  
### Step 8:
  Use a `for` loop from `i = 0` to `i < n` to:  
  - **Step 8.1:** Call the recursive function `fibo(i)`  
  - **Step 8.2:** Print the returned Fibonacci value  
### Step 9:
 Define the recursive function `fibo(x)` as follows:  
 - **Step 9.1:** If `x == 0` or `x == 1`, return `x`.  
 - **Step 9.2:** Otherwise, return `fibo(x - 1) + fibo(x - 2)`.  
### Step 10:
  Stop
# Program:
```
#include <stdio.h>

// Step 3: Declare recursive function
int fibo(int x);

int main() {
    // Step 4: Declare variables n and i
    int n, i;
    
    // Step 5 & 6: Prompt user and read the value of n
    printf("Enter a positive integer n: ");
    scanf("%d", &n);
    
    // Step 7: Display a message
    printf("Fibonacci series of %d terms:\n", n);
    
    // Step 8: Use a for loop to call fibo and print
    for (i = 0; i < n; i++) {
        printf("%d ", fibo(i));
    }
    printf("\n");
    
    return 0;
}

// Step 9: Define the recursive function
int fibo(int x) {
    // Step 9.1: Base case
    if (x == 0 || x == 1) {
        return x;
    } 
    // Step 9.2: Recursive call
    else {
        return fibo(x - 1) + fibo(x - 2);
    }
}
```
# Output:
<img width="287" height="156" alt="image" src="https://github.com/user-attachments/assets/c60b0a8c-8ab4-4dd0-9a61-add15532ba44" />

# Result: 
Thus, the program was implemented and executed successfully, and the required output was obtained.


# 19AI304-Fundamentals-of-C-Programming-2025-Odd-M5
# IAPR-5- Module 5 - FoC
# Ex.No:23
   Implement a C program to demonstrate recursion by printing a sequence of even or odd numbers from a given lower limit to an upper limit, with each recursive call progressing by 2.
# Date : 10/09/26
# Aim:
  To implement a C program that uses a recursive function to print even or odd numbers in a specified range based on the starting value provided by the user.
# Algorithm:
### Step 1:
  Start
### Step 2: 
  Include the standard input-output library: #include<stdio.h>. 
### Step 3:
  Declare a recursive function `printEvenOdd(int cur, int limit)` to print numbers from `cur` to `limit` with a step of 2.
### Step 4:
  In the `main()` function, declare two integer variables: `lowerLimit` and `upperLimit`.
### Step 5:
  Prompt the user to enter the lower limit of the range.
### Step 6:
  Read and store the lower limit.
### Step 7:
  Prompt the user to enter the upper limit of the range.
### Step 8:
  Read and store the upper limit.
### Step 9:
  Display a message indicating that the even/odd numbers in the given range will be printed.
### Step 10:
  Call the recursive function `printEvenOdd(lowerLimit, upperLimit)`.
### Step 11:
  Inside the function `printEvenOdd(cur, limit)`:
  - **Step 11.1:** If `cur > limit`, terminate the recursion.  
  - **Step 11.2:** If `cur == limit`, print the value without a trailing comma.  
  - **Step 11.3:** Otherwise, print the current value followed by a comma.  
  - **Step 11.4:** Recursively call `printEvenOdd(cur + 2, limit)` to print the next number.
### Step 12:
  Stop
# Program:
```
#include <stdio.h>

// Step 3: Declare recursive function
void printEvenOdd(int cur, int limit);

int main() {
    // Step 4: Declare variables
    int lowerLimit, upperLimit;
    
    // Step 5 & 6: Prompt and read lower limit
    printf("Enter the lower limit: ");
    scanf("%d", &lowerLimit);
    
    // Step 7 & 8: Prompt and read upper limit
    printf("Enter the upper limit: ");
    scanf("%d", &upperLimit);
    
    // Step 9: Display message
    printf("Even/Odd numbers from %d to %d are:\n", lowerLimit, upperLimit);
    
    // Step 10: Call the recursive function
    printEvenOdd(lowerLimit, upperLimit);
    printf("\n");
    
    return 0;
}

// Step 11: Inside the function
void printEvenOdd(int cur, int limit) {
    // Step 11.1: Terminate recursion
    if (cur > limit) {
        return;
    }
    
    // Step 11.2: Print without trailing comma if it's the last element
    if (cur == limit || cur + 2 > limit) {
        printf("%d", cur);
    } 
    // Step 11.3: Otherwise, print followed by comma
    else {
        printf("%d, ", cur);
    }
    
    // Step 11.4: Recursively call for next number
    printEvenOdd(cur + 2, limit);
}
```
# Output:
<img width="518" height="192" alt="image" src="https://github.com/user-attachments/assets/3b1fee9f-a748-4a1f-8ed5-66e412e6b418" />

# Result: 
Thus, the program was implemented and executed successfully, and the required output was obtained.


# 19AI304-Fundamentals-of-C-Programming-2025-Odd-M5
# IAPR-5- Module 5 - FoC
# Ex.No:24
   Implement a C program that dynamically allocates memory using calloc(), accepts integer inputs from the user, computes their sum, and prints the sum.
# Date : 10/9/26
# Aim:
  To implement a C program that dynamically allocates memory for an array of integers using calloc(), accepts elements from the user, computes their sum, and displays the sum.
# Algorithm:
### Step 1:
  Start
### Step 2: 
  Include the standard input-output library: #include<stdio.h>. 
### Step 3:
  a. Declare a pointer `ptr` to `int`.  
  b. Declare integers `n`, `i`, and `sum` (initialize `sum = 0`).
### Step 4:
  Read the integer `n` from the user (the number of integers to be stored).
### Step 5:
  Use the `calloc()` function to allocate memory for `n` integers:  
  `ptr = calloc(n, sizeof(int))`
### Step 6:
  If `ptr` is not `NULL`, continue to the next step; otherwise, memory allocation failed (the program exits).
### Step 7:
  For each `i` from `0` to `n - 1`:  
  a. Read an integer from the user.  
  b. Store it at memory location `ptr + i`.
### Step 8:
  For each `i` from `0` to `n - 1`:  
  a. Access the value stored at `ptr + i`.  
  b. Add it to `sum`.
### Step 9:
  Print the value of `sum`.
### Step 10:
  Call `free(ptr);` to release the memory allocated by `calloc()`.
### Step 11:
  Stop
# Program:
```
#include <stdio.h>
#include <stdlib.h> // Required for calloc and free

int main() {
    // Step 3: Declare pointer and variables
    int *ptr;
    int n, i, sum = 0;
    
    // Step 4: Read the integer n
    printf("Enter the number of integers to store: ");
    scanf("%d", &n);
    
    // Step 5: Allocate memory using calloc
    ptr = (int *)calloc(n, sizeof(int));
    
    // Step 6: Check if memory allocation failed
    if (ptr == NULL) {
        printf("Memory allocation failed.\n");
        return 1; // Program exits
    }
    
    // Step 7: Read elements from user
    printf("Enter %d integers:\n", n);
    for (i = 0; i < n; i++) {
        scanf("%d", ptr + i); // Store at memory location ptr + i
    }
    
    // Step 8: Compute sum
    for (i = 0; i < n; i++) {
        sum = sum + *(ptr + i); // Access value at ptr + i
    }
    
    // Step 9: Print the sum
    printf("Sum of the elements: %d\n", sum);
    
    // Step 10: Release memory
    free(ptr);
    
    return 0;
}
```
# Output:
<img width="302" height="207" alt="image" src="https://github.com/user-attachments/assets/9e053053-c329-4a10-8e52-188ead54c9b8" />

# Result: 
Thus, the program was implemented and executed successfully, and the required output was obtained.


# 19AI304-Fundamentals-of-C-Programming-2025-Odd-M5
# IAPR-5- Module 5 - FoC
# Ex.No:25
   Implement a C program that reads a set of integers into an array and displays the array elements using a user-defined function.
# Date : 10/09/26
# Aim:
  To implement a C program that reads integers into an array and displays the elements using a user-defined function.
# Algorithm:
### Step 1:
  Start
### Step 2: 
  Include the standard input-output library: #include<stdio.h>. 
### Step 3:
  Declare the function prototype: `void displayArray(int *arr, int size);`
### Step 4:
  In the `main()` function, declare an integer array of size 5 and a loop variable.
### Step 5:
  Prompt the user to enter the required number of integers.
### Step 6:
  Read the integers from the user and store them in the array using a loop.
### Step 7:
  Call the `displayArray` function, passing the array and its size as arguments.
### Step 8:
  Define the function `displayArray(int *arr, int size)` to print the array elements:  
  - Loop through the array using either pointer arithmetic (`*(arr + i)`) or array indexing (`arr[i]`).  
  - Print each element.
### Step 9:
  Return to the `main()` function after displaying the array.
### Step 10:
  Stop
# Program:
```
#include <stdio.h>

// Step 3: Declare function prototype
void displayArray(int *arr, int size);

int main() {
    // Step 4: Declare an integer array of size 5 and a loop variable
    int array[5];
    int i;
    int size = 5;
    
    // Step 5: Prompt user
    printf("Enter %d integers:\n", size);
    
    // Step 6: Read integers and store in array
    for (i = 0; i < size; i++) {
        scanf("%d", &array[i]);
    }
    
    // Step 7: Call the displayArray function
    displayArray(array, size);
    
    return 0;
}

// Step 8: Define the displayArray function
void displayArray(int *arr, int size) {
    int i;
    printf("The elements of the array are:\n");
    // Loop through the array using pointer arithmetic
    for (i = 0; i < size; i++) {
        printf("%d ", *(arr + i));
    }
    printf("\n");
    // Step 9: Returns automatically at the end of void function
}
```
# output:
<img width="322" height="250" alt="image" src="https://github.com/user-attachments/assets/45c7e8e9-e27c-4319-b365-8db19665cdfc" />
# Result:
Thus, the program was implemented and executed successfully, and the required output was obtained.


# Output:
# Result: 
Thus, the program was implemented and executed successfully, and the required output was obtained.
