#include <stdio.h>

int main() {
    char filename[100];
    FILE *fp;
    int ch;

    printf("Enter filename: ");
    scanf("%s", filename);

    // Try opening file in read mode
    fp = fopen(filename, "r");

    if (fp == NULL) {
        printf("Error: File '%s' does not exist or cannot be opened.\n", filename);
        return 1;
    }

    printf("\n--- File Content ---\n");

    // Read and print file content character by character
    while ((ch = fgetc(fp)) != EOF) {
        putchar(ch);
    }

    fclose(fp);

    return 0;
}
