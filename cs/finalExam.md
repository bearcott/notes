#Final Exam Cramming

**TOC**
- [Lesson 13 Classes](#lesson-13)
- [Lesson 14 More Classes](#lesson-14)
- [Lesson 15 Inheritance & Polymorphism](#lesson-15)
- [Lesson 16 Exceptions](#lesson-16)

----------------------------------------------------------------------------

###Lesson 11 (not on test)
**abstract data type** are values that can be stored, operations that can be done on values. Users dont need to know how its stored. Its created by programmers.

**abstraction** captures the general detail without details.

###Lesson 13
**class** like `struct` allows bundling of related variables, has also functions.
- like struct, also requires a finishing semicolon.

**object** an instance of a class, like a variable is an instance of a class.
- *attributes* members of class
- *methods/behaviors* member functions of class

**data hiding** restricting access to certain members of an object

**static** one variable shared among all objects of a class

- must be declared inside function and defined outside
- if no value is set, default is 0.

*there will be a compile error if you try to access a private member* 

    Class::name //creates

    Class.name(); //uses
    Class->name(); //if its a pointer

**regular functions** called -> stores address of call, allocates memory for local variable, etc.

**inline functions** larger executable program but no function call overhead. *faster*

**constructor** called when a class is initiated
- overloaded constructors is when you have more than one.

**default constructor** is a constructor that takes no argument or a constructor with default arguments.
- when they all require arguments, then there is no default constructor
- other member functions can be overloaded.
- In order to overload, you just have a unique parameter list

    void setConst(double);
    void setConst(int *);

    Rectangle(double = 0, int = 0);
    Rectangle r; //would cause the above to execute;
    Rectangle r(1,1); works too.

**destructor** its called when object is destroyed.
- only one destrucor per class, *cannot* be overloaded.
- if constructor does allocates dynamic memory, destructor should release it.

    classname::~classname //destroys
    {
        delete [] stuff; //deletes allocated array of memory
    }

**array of objects**

    someclass somearray[2] = {someclass(2,3),someclass()};

**UML** Unified Modeling Language - used for writing classes
- private are indicated with a minus. Public indicated with a plus.
- datatype indicated with colon

    - private
    + public : double
    + public(name : int) : void

###Lesson 14

*variable types*
**instance variable** member variable in a class. Each class has a copy.

**static variable** one variable shared amongst all objects of a class. 

**static member function** can be used to access `static variables` can be called before objects are defined. *can only access static data*

*all static must be initialized out of line*

    class someclass
    {
    private:
        double length;
        static int count; //static member
    public:
        static int getCount(); //static member function
    };
    int someclass:count = 3;

**Friend** is a function or class that is not a member of a class, but has access to private members of the class.

- declared with the `friend` keyword.

Ex.

    class FriendClass
    {
        ...
    };
    int getCount() {
        return NewClass::count;
    }
    class NewClass
    {
        static int count = 3;
    public:
        friend class FriendClass;
        friend int getCount();
    };

**copy constructors** when initializing one class with the data of another, something special happens.
- it copies the object field to field.
- when working with pointers, the object makes a dynamic member reference.

    SomeClass object1(5);
    SomeClass object2 = object1;
    object2.setVal(13);
    cout << object1.getVal(); // also 13 if pointer

*default works fine, but in the case of having a pointer, a special copy constructor is needed in order to let them have seperate pointer instead of a `dynamic member reference`*

    SomeClass::SomeClass(const SomeClass &obj)
    {
        value = new int;
        *value = obj.value;
    }

**overloaded operators**
Can do most operators except:

    ?: . .* :: sizeof

Required that you use the `operator` keyword:

    operator+ //for the + operator

    //in use:
    class getParameter
    {
        int x;
        public:
            getParameter(int newx) {
                x = newx;
            }
            double operator+(const getParameter &other)
            {
                return 2 * x + 2 * other.x;
            }
    }
    getParameter one(2), two(4);
    cout << one + two; // 2*2 + 2*4


- `++` and `--` still work as prefix, postfix.
    + Does it work like 
- overloaded relational operators should *return a bool value*
- overloaded stream operators `>>`,`<<` must reference istream, ostream and use istream, ostream as parameters as well.
- overloaded `[]`
    + can create classes that behave like arrays: benefit is can make bounds check.
    + must also consider constructor, destructor
    + it returns a reference to object, not the object itself.

**this** is always availabe as  a predefined member function for all classes.

- it always points to the object/instance (not the class itself)
- can be used in all *non-static* functions
- can be used to access members that may be hidden by parameters that have the same name.

Ex.

    class someClass 
    {
        int num;
    public:
        void setNum(int newNum)
        {
            this->num = newNum;
        }
    }

**aggregation** is concept of a class within a class.

    class StudentInfo 
    {...};
    class Student
    {
         private:
                StudentInfo personalData;
        ...
    };

###Lesson 15
**inheritance** provides a way to create new, specialized classes from existing classes.

    class Animal
    {...};

    //class <name> : <access level> <class name(params)>
    class JohnCole : public Animal  
    {...};

- works like **base class** which will have a **derived class**

a **derived class** 

- has all members of child and parent class
- can use all members of child and parent class *under `public`*
- can have their own consructors and destructors
    + the base classes constructors are executed first, then derived class.
    + the derived classes destructors are executed first, then base class.
- can have multiple base classes, each having its own access level.

    class cube : public square, public colors

**class access**

- **public** public objects of base become public objects of derived.
    + meaning derived can use, and outside can.

- **protected** public objects of base become protected members of derived.
    + meaning..

- **private** public members of base become private members of derived.
    + meaning derived can use, but outside cannot.

- the base class protection level.

**static binding** function calls are bound at compile time

- basically when you have functions `x()` and `y()` where `x()` calls `y()` in a class and you redefine `y()` in a derived class, calling function `x()` will call the original `y()` not the redefined one.
- this is the default way all C++ functions run.

**virtual member function** is a function from the base class that expects to be redefined

- its defined with the keyword `virtual` and supports **dynamic binding** meaning they are bound at runtime to th function they call (not compile time)
- when this object *must* be overridden in derived classes it is called a `pure virtual function.`
    + must have no function definitions in base class.

    virtual void Y() {...} //virtual function
    virtual void Y() {...} = 0 //pure virtual function

an **abstract base class** can have no objects, its purpose is to serve as a template for derived classes that could have objects.
- a class becomes abstract once it has a member function that is a pure virtual function.

When a base class has members that have the *same name* as the derived class's:
- derived class redefines these objects
- it invokes the member using a `scope resolution operator` aka `::`
- compile error if derived class tries to access base class functions.

###Lesson 16
**exceptions** this is a way to safely handle errors

- if a function `throws` an exception the function terminates and the `try` block looks for a `catch` block with the same exception which executes if found then exits.
    + the value obtained from a catch block *does not* need to be used.
    + all functions can throw exceptions even predefined ones like `new`
- Once the exception is thrown the program does not return to the `throw` all called functions terminate in try block, resulting in **unwinding the stack**
    + all objects created in try blcok are now destroyed.
- try blocks can be nested.

Ex. 

    try 
    {
        ...
    }
    catch (char *msg) //if exception is a string, it jumps to catch
    {
        cout << "The error is " << msg;
    }

An exception will not be caught if:
- its thrown outside the try block
- there is no catch block that matches the data type.

**exception classes**

- can have no members, used onl to signal an error.
- or have members: pass errors to catch block
- a class can have multiple exception classes.

###Lesson 17
Recurson breaks down complex problems into easier to solve cases which is called a **base case** (recursion stops when base case is reached.)

- each iteration is known as a **stack frame**

Two types of recursion

- Direct: functions A -> A
- Indirect: functions A -> B -> A

Ex

    //GCD Largest factor the two integers have in common
    int gcd(int x, int y)
    {
        if (x % y == 0)
            return y;
        else
            return gcd(y, x % y);
    }
    //Factorial n(n-1)!
    int factorial (int num)
    {
    if (num > 0)
        return num * factorial(num - 1);
    else
        return 1;
    }
    //Fibonacci
    int fib(int n)
    {
        if (n <= 0)
            return 0;
        else if (n == 1)
            return 1;
        else
            return fib(n – 1) + fib(n – 2);
    }

Remember **quicksort** and **binary search**

**quicksort** one pivot point determined, sorts so that values to the left are less than values to right

**binary search** splits at pivot point, (requires sorted) then if greater than, checks left, repeat.

**Exhaustive algorithm** search a set of combinations to find an optimal one. (

e.g: Change that uses the least amount of coins.)




