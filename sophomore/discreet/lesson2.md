Table of common logical operations

|P|Q|P or Q|P and Q|P xor Q|P bicond Q|
|-|-|------|-------|-------|----------|
|0|0|0     |0      |0      |1         |
|0|1|1     |0      |1      |0         |
|1|0|1     |0      |1      |0         |
|1|1|1     |1      |0      |1         |

- NOT (¬)

- OR - if one is true, then true (v)
  - p or q.
- AND - both are true, then true (^)
  - p and q.
- XOR - one is false one is true, then true ((+))
  - p or q, but not both.
- Bi-conditional - both are false or true, then true (<->)
  - p if and only if q.
  - known as *IFF*

The expression `p -> q` is a *conditional statement* which shows that based off condition `p` implies `q`.
- true does not imply false but everything else works.

     if P, then Q.

**truth table operator precedence**
In order of most first:
- NOT
- AND
- OR
- ->
- <->

*if a logical expression is true for all values of its true table, then the expression is called a **tautology***

*if it is false for all is **contradiction***

*if it is conditionally true its **contingent***

|P|Q|PvQ|P->(PvQ)|
|-|-|---|--------|
|0|0|0  |1       |
|0|1|1  |1       |
|1|0|1  |1       |
|1|1|1  |1       |


**english examples**

Inclusive OR

    Students who have taken calculus or computer science can take this class.

Exclusive OR

    Students who have taken calculus or computer science, but not both, can enroll in this class.

A *bit string* is a sequence of zero or more bits. The length of this string is the number of bits in the string.
