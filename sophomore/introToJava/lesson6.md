# Single Dimension Arrays

    double[] myList = new double[5]

    double[] myList = {0.1,2.2}

    java.util.Arrays.sort(myList);

    Arrays.toString(list); //returns string representation

    Array.length

    new int[20] {1,2,3,4} //instant array

When an array is created it is given initial values:
- false for boolean
- 0 for numeric
- `\u0000` for characters

go through the full array

    for (double val : list)
      System.out.print(val)

**searches**
- linear (0 to 10)
- binary (5 then compare)

**sorts**
- selection sort (place lowest first, then second lowest)
- `java.util.Arrays.sort({})`

#Multidimension Arrays

    int[][] multiArray = new int[10][10]
    int[][] multiArray = {{1,2,3},{3,4,5}}
