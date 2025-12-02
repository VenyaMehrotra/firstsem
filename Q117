#include <stdio.h>

int main() {
    int n;
    scanf("%d", &n); // size of array
    
    int arr[n];
    for (int i = 0; i < n; i++)
        scanf("%d", &arr[i]);
    
    int xor_all = 0;
    
    // XOR all array elements and numbers from 1 to n-1
    // Because one number is repeated, XOR will cancel all except the duplicate
    for (int i = 0; i < n; i++) {
        xor_all ^= arr[i];
        xor_all ^= i;  // XOR with index (acts like XOR with numbers 0..n-1)
    }
    
    printf("%d\n", xor_all);
    return 0;
}
