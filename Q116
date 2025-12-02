#include <stdio.h>

int main() {
    int n;
    scanf("%d", &n); // input size (array has n elements but numbers range 0..n)

    int arr[n];
    for (int i = 0; i < n; i++)
        scanf("%d", &arr[i]);

    int total = n * (n + 1) / 2; // sum of 0..n
    int sum = 0;

    for (int i = 0; i < n; i++)
        sum += arr[i];

    printf("%d\n", total - sum); // missing number
    return 0;
}
