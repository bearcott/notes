# Proofs

- indirect proof
- proof by contradiction
- proof by math induction
- *non-constructive proof* (not tested)

## Indirect Proof

    Theorem:  let N be an int
              if N is odd then N^2 is odd

    Proof:    N is odd (given)
              N = 2K+1
              N^2 = 4K^2+4K+1
              N^2 = 2(2*K^2 + 2K)+1
              N^2 is odd Q.E.D (the proof is finished)

    Theorem:  If 3N+2 is odd then N is odd

    Proof:    3N+2 is odd (given)
              3N+2 = 2K+1 For Some int K
              2N = 2K-1
              N is odd

Thing to consider:
- `2 * INT = even`
  - hence `2N` and `2K` must be even
    - hence `2K - 1` must be odd


    Theorem:  Let N be a pos int
              If the sum of the digits of N is div of 3 then N is a div by 3.

    Proof:    For simplicity let N be a 4 digit number.
              N = ABCD
              A+B+C=D = 3K for some int K
              N = 1000A + 100B + 10C + D
              3K = A + B + C + D for any int K
              N - 3k = 999A + 99B + 9C
              N = 999A + 99B + 9C + 3k
              N = 3(333a + 33B + 3C + k)
              N is divisible by 3. Q.E.D

## Proof by contradiction

suppose you have proof `P->Q`

assume the negation of `P->Q`

idk..

    A number is rational if
    It can be written as a ratio of integers

    .264 = 264/1000

    the decimal expansion of a rational number either terminates on some digits at the end repeat
    -----------------------------------------
    An irrational number is one that is not rational decimal expansion has no end and does not repeat

Time for a proof *THERE IS A SIMILAR QUESTION LIKE THIS ON THE EXAM*

    Theorem:  The square root of 2 is irrational.

    Proof:    Assume (2)^0.5 is rational
              (2)^0.5 = B/C, where B/C is the simplest form.
              2=B^2/C^2
              B^2 = 2C^2
              B^2 is even
              B is even
              B = 2K for some int K
              B^2 = 4K^2

## Non constructive proof

    Theorem:  If X is irrational and Y is irrational
              Then X^Y is irrational.

    Proof:    (2)^0.5 is irrational
              consider (2)^(2^0.5)
              (2)^2 = 2 rational
              ExEy[x^y is rational
              ^ non constructive
