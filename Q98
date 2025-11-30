#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main() {
    char name[200];
    char *token, lastName[50];
    int count = 0;

    printf("Enter your full name: ");
    fgets(name, sizeof(name), stdin);

    // Remove trailing newline if present
    name[strcspn(name, "\n")] = '\0';

    // Split name into words
    token = strtok(name, " ");
    while (token != NULL) {
        count++;

        // Store the last token (surname)
        strcpy(lastName, token);

        // Print initial for all but last name
        if (strtok(NULL, " ") != NULL) {
            printf("%c. ", toupper(token[0]));
            // move back one token so loop continues correctly
            token = strtok(NULL, " ");
            continue;
        }

        token = strtok(NULL, " ");
    }

    // Now print surname in full
    printf("%s\n", lastName);

    return 0;
}
