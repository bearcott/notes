#Test
questions
- multiple choice
- 2 programming
- 5 mins early
- chapters 1-10

**Aggregate & Composition**
- you can make a class inside a class
- or put other classes inside ur class

    java.math.BigInteger

    BigInteger a = new BigInteger(22342342);
    BigInteger b = new BigInteger(141241241);
    a.multiply(b);

- they extend the number class implement comparable interface
- immutable

*Because strings are immutable, if the same string is used twice then no new object is created*
- this is called an interned instance

**regex**
- 'str1i@n3g'.replaceAll('[1@3]',' ') //replaces 1 @ and 3 with ' '

for mutableish strings use `StringBuilder` or `StringBuffer`

**Abstract Classes**
- does not get initiated using a `new` keyword, however still uses constructors.
- subclasses can override superclass methods to be abstract
- this can be used as a data type, so you can make an array using `new` keyword

    AbstractClass taco = new AbstractClass[10];
