#include <stdio.h>

struct Person {
    char name[30];
    int age;
    float salary;
};

int main() {
    struct Person p;          // Normal structure variable
    struct Person *ptr;       // Pointer to structure

    ptr = &p;                 // Point pointer to structure variable

    // Taking input using -> operator
    printf("Enter Name: ");
    scanf(" %[^\n]s", ptr->name);

    printf("Enter Age: ");
    scanf("%d", &ptr->age);

    printf("Enter Salary: ");
    scanf("%f", &ptr->salary);

    // Modifying values using pointer
    ptr->age += 2;             // Increase age by 2
    ptr->salary += 5000;       // Add bonus

    // Displaying using -> operator
    printf("\n--- Updated Person Details ---\n");
    printf("Name   : %s\n", ptr->name);
    printf("Age    : %d\n", ptr->age);
    printf("Salary : %.2f\n", ptr->salary);

    return 0;
}
