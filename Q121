#include <stdio.h>
#include <ctype.h>

int main() {
    char filename[100];
    FILE *fp;
    int ch;

    int characters = 0;
    int words = 0;
    int lines = 0;

    int inWord = 0;  // To track if we are inside a word

    printf("Enter filename: ");
    scanf("%s", filename);

    fp = fopen(filename, "r");
    if (fp == NULL) {
        printf("Error: Could not open file.\n");
        return 1;
    }

    while ((ch = fgetc(fp)) != EOF) {
        characters++;

        if (ch == '\n')
            lines++;

        if (!isspace(ch)) {
            if (inWord == 0) {
                words++;
                inWord = 1;
            }
        } else {
            inWord = 0;
        }
    }

    fclose(fp);

    printf("\n--- File Statistics ---\n");
    printf("Characters: %d\n", characters);
    printf("Words: %d\n", words);
    printf("Lines: %d\n", lines);

    return 0;
}
