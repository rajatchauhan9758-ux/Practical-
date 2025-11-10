# Practical-
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int user, computer;
    srand(time(0));

    printf("Choose:\n1. Rock\n2. Paper\n3. Scissors\n");
    scanf("%d", &user);

    computer = rand() % 3 + 1;

    // Display user choice
    if (user == 1) {
        printf("You chose Rock\n");
    } else if (user == 2) {
        printf("You chose Paper\n");
    } else if (user == 3) {
        printf("You chose Scissors\n");
    } else {
        printf("Invalid choice!\n");
        return 0;
    }

    // Display computer choice
    if (computer == 1) {
        printf("Computer chose Rock\n");
    } else if (computer == 2) {
        printf("Computer chose Paper\n");
    } else {
        printf("Computer chose Scissors\n");
    }

    // Game logic
    if (user == computer) {
        printf("It's a draw!\n");
    } 
    else if (user == 1 && computer == 3) {
        printf("Rock wins over Scissors — You win!\n");
    } 
    else if (user == 2 && computer == 1) {
        printf("Paper wins over Rock — You win!\n");
    } 
    else if (user == 3 && computer == 2) {
        printf("Scissors win over Paper — You win!\n");
    } 
    else if (computer == 1 && user == 3) {
        printf("Rock wins over Scissors — You lose!\n");
    } 
    else if (computer == 2 && user == 1) {
        printf("Paper wins over Rock — You lose!\n");
    } 
    else if (computer == 3 && user == 2) {
        printf("Scissors win over Paper — You lose!\n");
    }

    return 0;
}
