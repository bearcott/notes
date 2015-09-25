## LU Factorization

- Since `A = LU` then `LUx = b`
- Write `y = Ux` and solve `Ly = b` for `y`
- Solve `Ux = y` for `x`

# Chapter 3

**determinant**

a 1x1 matrix is the determinant of itself.

The determinant of a *square matrix* greater than a 1x1 is the sum of the entries in the first row multiplied by its cofactor.

**minor and cofactor**

**minor** is the result of deleting a column and a row and then finding the determinant of the remaining stuff.

    Mij is the result of deleting row i and column j then finding the determinant of the remaining rows/columns

**cofactor** is the resulting number from a minor possibly with flipped sign.

    if i + j is even -> Cij = Mij
    if i + j is odd -> Cij = -Mij

**triangular matrices**

If A is a triangular matrix hen the det of A is the product of the main diagonal.

        [1 0 0]
    A = [2 2 0]
        [4 2 1]

    detA = (1)(2)(1) = 2
