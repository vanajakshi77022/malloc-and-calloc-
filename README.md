# malloc-and-calloc-
#include <stdio.h>
#include <stdlib.h>

int main() {
    int n, i;
    printf("25331A05E8\n");
    printf("Enter number of elements: ");
    scanf("%d", &n);

    // Using malloc
    int *arr1;
    arr1 = (int *)malloc(n * sizeof(int));

    if (arr1 == NULL) {
        printf("Memory allocation failed using malloc\n");
        return 1;
    }

    printf("\nEnter %d elements for malloc array:\n", n);
    for(i = 0; i < n; i++) {
        scanf("%d", &arr1[i]);
    }

    printf("Elements using malloc:\n");
    for(i = 0; i < n; i++) {
        printf("%d ", arr1[i]);
    }

    // Using calloc
    int *arr2;
    arr2 = (int *)calloc(n, sizeof(int));

    if (arr2 == NULL) {
        printf("Memory allocation failed using calloc\n");
        return 1;
    }

    printf("\n\nElements using calloc (default initialized to 0):\n");
    for(i = 0; i < n; i++) {
        printf("%d ", arr2[i]);
    }

    // Free allocated memory
    free(arr1);
    free(arr2);

    return 0;
}
