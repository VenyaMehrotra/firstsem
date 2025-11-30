#include <stdio.h>
#include <string.h>

int main() {
    char str[200];
    char word[50], longest[50];
    int i = 0, j = 0, maxLen = 0, len = 0;

    printf("Enter a sentence:\n");
    fgets(str, sizeof(str), stdin);

    // Remove newline if present
    str[strcspn(str, "\n")] = '\0';

    while (str[i] != '\0') {
        // If character is not a space, add to current word
        if (str[i] != ' ' && str[i] != '\t') {
            word[j++] = str[i];
        } else {
            word[j] = '\0';  // end of current word
            len = strlen(word);
            if (len > maxLen) {
                maxLen = len;
                strcpy(longest, word);
            }
            j = 0;  // reset for next word
        }
        i++;
    }

    // For the last word (if sentence doesn't end with space)
    word[j] = '\0';
    len = strlen(word);
    if (len > maxLen) {
        maxLen = len;
        strcpy(longest, word);
    }

    printf("\nLongest word: %s\n", longest);
    printf("Length: %d\n", maxLen);

    return 0;
}
