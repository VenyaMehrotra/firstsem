#include <stdio.h>

int main() {
    int n, i, j;
    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    printf("Enter %d elements:\n", n);
    for(i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    printf("Previous greater elements: ");
    for(i = 0; i < n; i++) {
        int prevGreater = -1;

        // Check all elements to the left of arr[i]
        for(j = i - 1; j >= 0; j--) {
            if(arr[j] > arr[i]) {
                prevGreater = arr[j];
                break; // Stop at the nearest greater element
            }
        }

        printf("%d", prevGreater);

        if(i != n - 1)  // For comma separation
            printf(", ");
    }

    return 0;
}
