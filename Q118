#include <stdio.h>
#include <ctype.h>
#include <string.h>

int main() {
    char str[200];
    
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);

    // Convert entire string to lowercase first
    for (int i = 0; str[i]; i++) {
        str[i] = tolower(str[i]);
    }

    // Capitalize first letter of sentence if alphabet
    if (isalpha(str[0])) {
        str[0] = toupper(str[0]);
    }

    // Capitalize letter after '.', '!' or '?'
    for (int i = 1; str[i]; i++) {
        if ((str[i-1] == '.' || str[i-1] == '!' || str[i-1] == '?') && str[i] == ' ') {
            if (isalpha(str[i+1])) {
                str[i+1] = toupper(str[i+1]);
            }
        }
    }

    printf("Sentence case: %s", str);

    return 0;
}
