#include <stdio.h>
#include <string.h>

int main() {
    char str[200];
    char word[50];
    int i = 0, j = 0, k;

    printf("Enter a sentence:\n");
    fgets(str, sizeof(str), stdin);

    // Remove newline if present
    str[strcspn(str, "\n")] = '\0';

    printf("\nReversed words:\n");

    while (str[i] != '\0') {
        if (str[i] != ' ' && str[i] != '\t') {
            // collect current word
            word[j++] = str[i];
        } else {
            // end of a word → print it reversed
            word[j] = '\0';
            for (k = j - 1; k >= 0; k--)
                printf("%c", word[k]);
            printf(" ");
            j = 0; // reset for next word
        }
        i++;
    }

    // print the last word (if sentence doesn't end with space)
    word[j] = '\0';
    for (k = j - 1; k >= 0; k--)
        printf("%c", word[k]);

    printf("\n");
    return 0;
}
