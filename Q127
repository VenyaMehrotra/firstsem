#include <stdio.h>

int main() {
    FILE *fin, *fout;
    char ch;

    fin = fopen("input.txt", "r");
    fout = fopen("output.txt", "w");

    if (fin == NULL || fout == NULL) {
        printf("File error\n");
        return 1;
    }

    while ((ch = fgetc(fin)) != EOF) {
        if (ch >= 'a' && ch <= 'z') {
            ch = ch - 32;
        }
        fputc(ch, fout);
    }

    fclose(fin);
    fclose(fout);

    return 0;
}
