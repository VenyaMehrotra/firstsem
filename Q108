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

    printf("Enter value of k: ");
    scanf("%d", &k);

    if(k > n || k <= 0) {
        printf("Invalid input for k.");
        return 0;
    }

    int maxSum = -1000000; // A large negative number to start with

    // Brute force: check all subarrays of size k
    for(i = 0; i <= n - k; i++) {
        int currentSum = 0;
        for(j = i; j < i + k; j++) {
            currentSum += arr[j];
        }

        if(currentSum > maxSum)
            maxSum = currentSum;
    }

    printf("Maximum sum of subarray of size %d is: %d", k, maxSum);

    return 0;
}
