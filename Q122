#include <stdio.h>
#include <string.h>
#include <stdlib.h>

int main(void) {
    char src_name[260];
    char dst_name[260];

    /* Get source filename */
    printf("Enter source filename: ");
    if (!fgets(src_name, sizeof(src_name), stdin)) {
        fprintf(stderr, "Failed to read source filename.\n");
        return 1;
    }
    src_name[strcspn(src_name, "\n")] = '\0'; /* remove newline */

    /* Get destination filename */
    printf("Enter destination filename: ");
    if (!fgets(dst_name, sizeof(dst_name), stdin)) {
        fprintf(stderr, "Failed to read destination filename.\n");
        return 1;
    }
    dst_name[strcspn(dst_name, "\n")] = '\0'; /* remove newline */

    /* Prevent overwriting the same file */
    if (strcmp(src_name, dst_name) == 0) {
        fprintf(stderr, "Source and destination are the same. Aborting to avoid data loss.\n");
        return 1;
    }

    /* Open files in binary mode so it works for text and binary files */
    FILE *src = fopen(src_name, "rb");
    if (!src) {
        perror("Error opening source file");
        return 1;
    }

    FILE *dst = fopen(dst_name, "wb");
    if (!dst) {
        perror("Error opening/creating destination file");
        fclose(src);
        return 1;
    }

    /* Copy byte by byte */
    int ch;
    long copied = 0;
    while ((ch = fgetc(src)) != EOF) {
        if (fputc(ch, dst) == EOF) {
            perror("Write error");
            fclose(src);
            fclose(dst);
            return 1;
        }
        copied++;
    }

    if (ferror(src)) {
        perror("Read error");
        fclose(src);
        fclose(dst);
        return 1;
    }

    fclose(src);
    fclose(dst);

    printf("Copied %ld bytes from '%s' to '%s'.\n", copied, src_name, dst_name);
    return 0;
}
