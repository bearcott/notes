# CH1.2
### matrices
- *coefficient matrix* made from just coefficients
- *augmented matrix* is made from solutions and matrix.

Elementary matrix operations (same as equations operations)
- interchange two matrices
- multiply an matrix by a nonzero constants
- add a multiple of an matrix to another equation.

matrix is in *row echelon form* if
- all rows filled with zeros are put at the bottom
- each row's first number (called the leading 1) should be 1.
- for each row, leading one is more to the left as u progress.

e.g

    [1 4 5 6 | 1]
    [0 1 3 2 | 3]
    [0 0 0 1 | 4]
    [0 0 0 0 | 2]

*it is RREF if there are 0s on both sides of the 1.*

a **homogenious** system is when the solution is 0 for each row.
- these are always consistent

When an entire row except for the solution number is 0 then the system is *inconsistent* and has *no solution.* (example is above)

When there aren't enough rows to cover solutions, then there are *infinitely many solutions*
- you will have to use `t` or a substitute variable for this.

e.g

    [1 0 3 | 2]
    [0 1 5 | 3]
