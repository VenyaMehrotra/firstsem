#include <stdio.h>
#include <string.h>

int main() {
    char str[100];
    printf("Enter a string: ");
    gets(str);

    int len = strlen(str);

    // Outer loop for start index
    for (int i = 0; i < len; i++) {
        // Inner loop for end index
        for (int j = i; j < len; j++) {
            // Print from str[i] to str[j]
            for (int k = i; k <= j; k++)
                printf("%c", str[k]);
            printf("\n");
        }
    }
    return 0;
}
