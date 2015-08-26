**named constants**

    final datatype CONSTANTNAME = VALUE;
    final double PI = 3.14159; //this value cannot change.

**symantics**
- classname - ClassThing
- constantname  - CONSTANT_THING

**integer operations**
- 5/2 = 2
- 5.0/2 = 2.5
- *calculations involving floating point numbers are approximated since its not stored accurately.*
  - doubles are more accurate than floating points (16 digits vs 7 digits)
- java uses arithmetic order.
- parenthesis has precedence over *everything* e.g 10 + (++i) will first increment i.

**type conversion**

- If one of the operands is double, the other is converted into double.
- Otherwise, if one of the operands is float, the other is converted into float.
- Otherwise, if one of the operands is long, the other is converted into long.
- Otherwise, both operands are converted into int.


a **literal** is a number in a program e.g `g = 100 //100 is literal`

**literals**
- can convert `2.0` into a float (its default a double) by typing `2.0f` or `2.0F`
- scientific notation is allowed e.g `1.2345e+2`

`currentTime` from system returns time since midnight January 1, 1970.

**type casting**

    int i = (int)3.9; //fraction is truncated

**augmented type casting**

  int sum = 0;
  sum += 4.5 //equivilent of sum = (int)(sum + 4.5)

  
