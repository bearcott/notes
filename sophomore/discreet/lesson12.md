**algos** an algorithm is a finite sequence of well defined instructions that solves a problem.


*can you do an algo for the following?*

given a well defined problem is there an algorithm to solve it
- this is impossible

given a java program, make the shortest version of this program
- cant be done

given a problem that does have an algorithm to solve it what is the fastest algorithm to solve it?
- nope

some problems require an exponential amount of time to execute

*time for algorithms are measured by the number of instructions executed as a function of a dataset*
- **Big-O Notation** O(n^2)

Find greatest value in an unsorted array

    double find_greatest(double b[], int N) {
      double L = B[0]         // 1
      for (int i=1; i<N; i++) // N
        if(B[i] > L)          // N
          L = B[i];           // N
      return L                // 1
    }

- 3n+2 lines of code
- O(n)
  - so if u double n, then time it takes to execute doubles.
