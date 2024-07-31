# CalculatorProjectDoc
In this project of basic calculator in c language. All the fucnctionalities are mentioned in the main function itself. 

## Simple Calculator in C

### Overview
This project is a basic calculator implemented in C that performs simple arithmetic operations: addition, subtraction, multiplication, and division.

### Features
- **User Interaction**: Prompts the user to decide whether to use the calculator.
- **Operator Selection**: Allows the user to choose an arithmetic operator (+, -, *, /).
- **Input Handling**: Takes two floating-point numbers as input.
- **Operation Execution**: Performs the selected operation and displays the result.

### Code Explanation
1. **Header Inclusions**: Includes standard input-output and standard library headers.
   ```c
   #include <stdio.h>
   #include <stdlib.h>
   ```

2. **Main Function**: The entry point of the program.
   ```c
   int main() {
       float num_1, num_2;
       char cal, opr;
       printf("Want to use calculator?(Y/N) : \n");
       scanf("%c", &cal);
   ```

3. **User Decision**: Checks if the user wants to use the calculator.
   ```c
   if (cal == 'n' || cal == 'N') {
       printf("\nThank You !\n");
       exit(0);
   } else if (cal == 'y' || cal == 'Y') {
       printf("Choose an operator ( + , - , * , / ) : \n");
       scanf(" %c", &opr);
       printf("Enter the value of Number 1 : \n");
       scanf(" %f", &num_1);
       printf("Enter the value of Number 2 : \n");
       scanf(" %f", &num_2);
   ```

4. **Operation Execution**: Uses a switch-case to perform the selected operation.
   ```c
   switch (opr) {
       case '+':
           printf("Addition of Two Numbers :\n\n %.2f + %.2f = %.2f\n", num_1, num_2, (num_1 + num_2));
           break;
       case '-':
           printf("Subtraction of Two Numbers :\n\n %.2f - %.2f = %.2f\n", num_1, num_2, (num_1 - num_2));
           break;
       case '*':
           printf("Multiplication of Two Numbers :\n\n %.2f * %.2f = %.2f\n", num_1, num_2, (num_1 * num_2));
           break;
       case '/':
           if (num_2 == 0) {
               printf("Cannot Divide by Zero !\n");
           } else {
               printf("Division of Two Numbers :\n\n %.2f / %.2f = %.2f\n", num_1, num_2, (num_1 / num_2));
           }
           break;
       default:
           printf("Invalid Operator \n");
           break;
   }
   ```

5. **Invalid Input Handling**: Manages invalid inputs for the calculator prompt.
   ```c
   } else if (cal != 'n' && cal != 'N' && cal != 'y' && cal != 'Y') {
       printf("Invalid input!\n");
   }
   printf("\n Thank You !\n");
   return 0;
   }
   ```

### Conclusion
This simple calculator project demonstrates basic user interaction, input handling, and arithmetic operations in C. It's a great starting point for beginners to understand fundamental programming concepts.
