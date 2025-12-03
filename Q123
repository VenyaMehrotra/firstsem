#include <stdio.h>

int main() {
    char filename[100];
    char text[500];
    
    printf("Enter the filename: ");
    scanf("%s", filename);

    // Clear the leftover newline from input buffer
    getchar();

    // Open file in append mode
    FILE *fp = fopen(filename, "a");
    if (fp == NULL) {
        printf("Error: Could not open the file.\n");
        return 1;
    }

    printf("Enter the line to append: ");
    fgets(text, sizeof(text), stdin);

    // Write the new text at the end
    fputs(text, fp);

    fclose(fp);

    printf("Text appended successfully.\n");

    return 0;
}
