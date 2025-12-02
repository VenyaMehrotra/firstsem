#include <stdio.h>

int main() {
    int n, k, i, j;
    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    printf("Enter %d elements:\n", n);
    for(i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    printf("Enter window size k: ");
    scanf("%d", &k);

    if(k > n || k <= 0) {
        printf("Invalid input for k.");
        return 0;
    }

    printf("Maximum elements of each subarray: ");
    for(i = 0; i <= n - k; i++) {
        int max = arr[i];

        // Find maximum in the current window
        for(j = i; j < i + k; j++) {
            if(arr[j] > max) {
                max = arr[j];
            }
        }

        printf("%d", max);
        if(i != n - k)
            printf(" ");
    }

    return 0;
}
