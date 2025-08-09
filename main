#include <math.h>
#include <stdio.h>
#include <stdbool.h>

void printDash() {
    printf("\"+\" For Addition\n");
    printf("\"-\" For Subtraction\n");
    printf("\"*\" For Multiplication\n");
    printf("\"/\" For Division\n");
    printf("\"^\" For Modulo\n");
}

float compute(float one, float two, char operation) {
    float answer;
    if (operation == '+') {
        answer = one + two;
    }
    else if (operation == '-') {
        answer = one - two;
    }
    else if (operation == '*') {
        answer = one * two;
    }
    else if (operation == '/') {
        if (two == 0) {
            printf("Cannot divide by zero. Error...\n"
                   "Defaulting to 0\n");
            return 0;
        }
        answer = one / two;
    }
    else if (operation == '^') {
        answer = pow(one, two);
    }
    else {
        printf("Invalid operator was selected. Error...\nDefaulting answer to zero\n");
        answer = 0;
    }
    return answer;
}


int main(void) {

    printf("Hello this is a program that will allow you to calculate two numbers\n\n");
    while (true) {
        float number1 = 0;
        float number2 = 0;
        char chosenOperation = "";
        char continueRunning = "y";
        printf("Enter the number you would like to compute\n");
        scanf(" %f", &number1);

        printf("Enter the sign of the operation that you would like performed\n");
        printDash();
        scanf(" %c", &chosenOperation);

        printf("Enter the second number you would like to compute\n");
        scanf(" %f", &number2);

        float answer = compute(number1, number2, chosenOperation);
        printf("The answer is %f\n\n", answer);

        printf("Would you like to continue: \n\"y\" for yes\n\"n\" for no\n");
        scanf(" %c", &continueRunning);
        if (continueRunning == 'y' || continueRunning == 'Y') {
            printf("Restarting...\n");
        }
        else if (continueRunning == 'n' || continueRunning == 'N') {
            printf("Goodbye...\n");
            break;
        }
        else {
            printf("Invalid letter, continuing...\n");
        }

    }
    return 0;
}
