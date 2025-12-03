#include <stdio.h>

int main() {
    FILE *fp;
    char line[100];

    // Open file in read mode
    fp = fopen("info.txt", "r");

    // Check if file opened successfully
    if (fp == NULL) {
        printf("Error opening file! Make sure info.txt exists.\n");
        return 1;
    }

    printf("Contents of info.txt:\n");

    // Read and print lines until EOF
    while (fgets(line, sizeof(line), fp) != NULL) {
        printf("%s", line);
    }

    // Close the file
    fclose(fp);

    return 0;
}
