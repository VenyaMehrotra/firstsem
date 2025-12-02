#include <stdio.h>
#include <string.h>

int main() {
    char s[100];
    printf("Enter a string: ");
    scanf("%s", s);

    int n = strlen(s);
    int lastIndex[256];  // To store last seen index of characters
    for (int i = 0; i < 256; i++)
        lastIndex[i] = -1;

    int maxLen = 0;  // Length of longest substring
    int start = 0;   // Starting index of current substring

    for (int i = 0; i < n; i++) {
        // If current character was seen before and is inside current window
        if (lastIndex[(int)s[i]] >= start)
            start = lastIndex[(int)s[i]] + 1;

        // Update last seen index of current character
        lastIndex[(int)s[i]] = i;

        // Update maximum length
        int currentLen = i - start + 1;
        if (currentLen > maxLen)
            maxLen = currentLen;
    }

    printf("Length of longest substring without repeating characters: %d\n", maxLen);
    return 0;
}
