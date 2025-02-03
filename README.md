// Online C compiler to run C program onl#include <stdio.h>

#include <stdio.h>
void askQuestion(char question[], char A[], char B[], char C[], char D[], char correctOption) {
    char userAnswer;
    printf("\n%s\n", question);
    printf("A. %s\n",A);
    printf("B. %s\n",B);
    printf("C. %s\n",C);
    printf("D. %s\n",D);
    printf("Your answer (A/B/C/D): ");
    scanf(" %c", &userAnswer);
    if (userAnswer == correctOption || userAnswer == correctOption + 32) {
        printf("Correct!\n");
    } else {
        printf("Wrong! The correct answer was %c.\n", correctOption);
    }
}

int main() {
    printf("Welcome to the C Quiz Game!\n"); 
    askQuestion("What is the output of 5 + 3 in C?",
                "53", "8", "Error", "Depends on compiler", 'B');
    askQuestion("Which of these is a valid loop in C?",
                "repeat-until", "foreach", "while", "do-end", 'C');
    askQuestion("What does 'int' represent in C?",
                "Integer", "Float", "Character", "Boolean", 'A');
    printf("\nGame Over! Thanks for playing.\n");
    return 0;
}
