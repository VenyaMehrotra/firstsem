#include <stdio.h>

int main() {
    FILE *fp;
    char name[50];
    int age;

    // Open file in write mode
    fp = fopen("info.txt", "w");

    // Check if file opened successfully
    if (fp == NULL) {
        printf("Error opening file!\n");
        return 1;
    }

    // Take input from user
    printf("Enter your name: ");
    fgets(name, sizeof(name), stdin);  // Use fgets for safer input

    printf("Enter your age: ");
    scanf("%d", &age);

    // Write data to file
    fprintf(fp, "Name: %sAge: %d\n", name, age);

    // Close the file
    fclose(fp);

    // Confirm message
    printf("Data successfully saved to info.txt\n");

    return 0;
}
