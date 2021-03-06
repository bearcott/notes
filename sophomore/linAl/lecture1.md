# Chapter 1.1

*linear* equations involve only constants and addition/subtraction

*nonlinear* equations involve everything else lol..

a **solution** of n variables involves n real numbers. When put together, these make up a **solution set**. To describe this, you need a *parametric representation.*

**free variables** can take on any real value.

**parametric representation**

if there is not enough information, adding another *parameter* such as `t` below is useful.

    x1 = 4-2*x2
    x1 = 4 - 2*t, x2 = t
    //where t is any real number

**systems of linear equations**

    a11x1 + a12 + .. = b1
    a21x1 + a22 + .. = b2

**systems of two equations in two variables**

    x + y = 3
    x - y = -1

For a system of linear equations only one of the following is true:
- it has one solution (consistent)
- it has infinite solutions (consistent)
- it has no solutions (inconsistent)

###solving systems of linear equations

**row echelon form**

     x - 2y + 3z = 9
    -x + 3y      = -4
    2x - 5y + 5z = 17

    x - 2y + 3z = 9
         y + 3z = 5
              z = 2

**back substitution** is the process where you substitute known values into other equations to find more values. Can be done with `z` above.

**operations that produce equivalent systems**
- interchange two equations
- multiply an equation by a nonzero constants
- add a multiple of an equation to another equation.

**guassian elimination** is the result of using these methods to obtain row echelon form.

**inconsistent solution example**

    x - 2y + 3z = 9
         y + 3z = 5
              0 = 2

**infinite solution example**

    x - 2y + 3z = 9
         y + 3z = 5
              0 = 0

there is no `z` hence `x3` will be a free variable. At this point you can use *parametric reprenstation* to find `x` and `y` but only relatively.
