CS2 C++ Notes
-------------
sai notes can be found on [here](https://onedrive.live.com/redir?resid=8CEACC82290B2CB%211118)

###Exam is:
- everything through arrays. CH1-8.
- multiple choice
- fillin the blank
- few writing code questions

###local/global variables
- *global variables* not contants are initiated with a 0 (numerics) or null (string, object)
- *static local variables* retain their contents between function calls. Their default init value is 0.

###functions
- **stubs** are test functions
- **drivers** are test functions that calls other functions

###arrays
- *global arrays* are initialized to 0 by default, else not initialized.
- C++ does not check if subscript is valid. You can use a subscript beyond bounds.
- if partialy initiated, the rest of the elems will be 0.
- character arrays are special

    char name[] = "Henry";
    cout << name << endl;

    \>> Henry

- can initialized array dynamically.

    int* square = new int[num,num];
    ...
    int num1 = 2, int num2 = 3;
    square[num1,num2] = 0;

###vectors
- use `array.push_back(<int>)` to add an element to a full array vector
- `array.pop_back(<int>)` to remove last element
- `array.clear()`

###searches

**linear search**
- *inefficient/slow* - examines N/2 of N element array on average
- *easy algo* array can be in any order

**binary search**
- splits the array down the middle. If left of middle is right, then examine left. other side likewise.
- requires an *ordered array*

###sorts

**bubble sort**
- orders first two elements, order second and third elements, repeat.
- *inefficient* easy to understand too

**selection sort**
- look for smallest num in array and exchange put in smallest slot repeat.
- *more efficient than bubble sort*
- takes N^2 examines.

###pointers
- use `&` before variables in order to get address (in hex) of address
- the *indirection operator* `*` makes it so you can access the value stored in the pointer
    
    int x = 25;
    int thing = &x;
    cout << *thing;

    \>> 25

- a **constant pointer** is a pointer made with an address that cannot point to anthing else

    int value = 22;
    int * const pointer = &value;

- can also make a constant pointer to a constant

    int value = 22;
    const int * const pointer = &value;

**dynamic memory allocation**
- use `new` operator to allocate memory.
- new returns address of memory location.
- use `delete` to free dynamic memory. *and only dynamic memory!*
