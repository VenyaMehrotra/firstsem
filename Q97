#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main(void) {
    char name[200];
    int i, len;
    int printed = 0;

    printf("Enter your full name: ");
    if (!fgets(name, sizeof name, stdin)) return 0;

    // remove trailing newline if present
    name[strcspn(name, "\n")] = '\0';

    len = (int)strlen(name);
    // skip leading spaces
    i = 0;
    while (i < len && name[i] == ' ') i++;

    if (i < len && name[i] != '\0') {
        // print first initial
        putchar((char)toupper((unsigned char)name[i]));
        printed = 1;
    }

    // scan for initials after spaces, handle multiple spaces
    for (; i < len; i++) {
        if (name[i] == ' ') {
            // skip any additional spaces
            int j = i + 1;
            while (j < len && name[j] == ' ') j++;
            if (j < len && name[j] != '\0') {
                putchar((char)toupper((unsigned char)name[j]));
                printed = 1;
            }
            i = j; // continue from j in next loop iteration
        }
    }

    if (!printed) {
        printf("\nNo initials found (empty input).\n");
    } else {
        printf("\n");
    }

    return 0;
}
