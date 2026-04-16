

Overview



Using pointer arithmetic (*(arr[i] + j))

Using standard array indexing (arr[i][j])

Both approaches produce the same output, showing how array indexing is built on pointer arithmetic.

Code Explanation

Array Initialization

int arr[3][4] = {
    {1, 2, 3, 4},
    {5, 6, 7, 8},
    {9, 10, 11, 12}
};

A 2D array with 3 rows and 4 columns is created.

It is filled with integers from 1 to 12.

Printing with Pointer Arithmetic

for (i = 0; i < ROW; i++) {
    for (j = 0; j < COL; j++) {
        printf("%4d", *(arr[i] + j));
    }
    printf("\n");
}

arr[i] gives the address of the i-th row.

arr[i] + j moves the pointer to the j-th element in that row.

*(arr[i] + j) dereferences the pointer, retrieving the value.

Printing with Normal Indexing

for (i = 0; i < ROW; i++) {
    for (j = 0; j < COL; j++) {
        printf("%4d", arr[i][j]);
    }
    printf("\n");
}

arr[i][j] directly retrieves the element at row i and column j.

Output

The program prints the same matrix twice:

>>> *(arr[i] + j) <<<
   1   2   3   4
   5   6   7   8
   9  10  11  12

>>> arr[i][j] <<<
   1   2   3   4
   5   6   7   8
   9  10  11  12

Key Takeaway

arr[i][j] and *(arr[i] + j) are equivalent.
