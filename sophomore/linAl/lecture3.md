### Polynomial Curve Fitting

    a0*x0^0 + a1*x0^1 + a2*x0^2 .. an*xn = y0
    a0*x1^0 + a1*x1^1 + a2*x1^2 .. an*xn = y1
    ..

Given coordinates `x` and `y` will yield an equation based on `n` degree polynomial.

*further intense thinking..*

I mean think about the normal polynomial.

    x^2 + 2x + 1;

It's basically

    a2x0^2 + a1x0 + a0x^0

This solves the coefficients of the polynomials by plugging in coordinates into a system of equations.

*Matlab e.g*

    >> A = [111;111;111];
    >> b = [1;1;1];
    >> rref([A b]);
    >> x=[0:0.001:3]; //range of 0 to 3 but in steps of .001
    >> plot(x, 2*x+x.^2);

If x values are too big, then you can make another variable to substitute it. e.g `z = x-2000;`

### Network Analysis
- networks are composed of junctions and branches.
- The sum of all junctions, and branches should be the same.

**Electrical Circuits**

Kirchoff's law:

1. All currents flowing into a junction (node) should be equal to all load flowing out.
2. The sum of the `RI` (resistance * current) products around a closed path (loop) is equal to the total `voltage`0 in the path.
