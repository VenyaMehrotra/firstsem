#include <stdio.h>
#include <stdlib.h>

struct Student {
    char name[30];
    int age;
    float marks;
};

int main() {

    struct Student *s;

    // Allocating memory for one Student structure
    s = (struct Student*) malloc(sizeof(struct Student));

    if (s == NULL) {
        printf("Memory allocation failed!\n");
        return 0;
    }

    printf("Enter Student Name: ");
    scanf(" %[^\n]s", s->name);

    printf("Enter Age: ");
    scanf("%d", &s->age);

    printf("Enter Marks: ");
    scanf("%f", &s->marks);

    printf("\n--- Student Details ---\n");
    printf("Name  : %s\n", s->name);
    printf("Age   : %d\n", s->age);
    printf("Marks : %.2f\n", s->marks);

    // Free allocated memory
    free(s);

    return 0;
}
