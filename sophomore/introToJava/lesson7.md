# Classes

- capitalize first letter
- **static classes** can be invoked without `new`



**constructors**

- MUST have the same name as the class itself
- do not have a return type (not void)
- constructors are invoked when `new` class is called

**variables**
- java does not assign default values to local variables inside a method (such as main)
- when creating a `new` object, the variable used is only a reference
  - if you do `a = b`, `b` will be reference to `a`
- *instance vs static*

**immutable** means cannot be changed once created

**this**
- instance variables must use this.

**garbage collection** by JVM if a variable is no longer used it is destroyed

**Random class**

    import java.util.Random;
    Random r = new Random(3); //random with seed.
    r.nextLong() //int, bool, float, long

**point2d**
