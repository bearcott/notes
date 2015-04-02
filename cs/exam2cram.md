#Exam 2 cram!!!!

**structs**

- structs must have a semi colon
- multiple variables can be declared in one line

e.g

    string name, address;

- struct does not allocate memory to create variables
- struct objects cannot be compared, only their methods.
- variables can be initialized when defined or after

e.g

    Student s = {11, "john"};
    s.name = "john";


- structs can be defined as arrays

e.g

    Student s[4]
    *this is actually an array of 4 structures*


- When dereferencing a pointer value 
- *when using a pointer* always use '->' instead of '.'

e.g

    S.name = "hello"; //normal
    ptrS->name = "hello"; // pointer

**unions**
- all members share a single memory location (cell)
- hence only *one* member is used at a time.
- basically single member structs.
- when declared outside a function must use static
- allocates memory *at declaration time*

**enumerators**

- basically

e.g

    enum week = {MONDAY,WEDNESDAY,FRIDAY};
    week mon = MONDAY;


- they are stored in memory as integers

e.g

    enum {MONDAY, WEDNESDAY, FIRDAY};


- cannot do mathematical operations on enums, can only use for comparision.
- Can define multiple variables using same enum expression

e.g 

    enum Car { PORSCHE, FERRARI, JAGUAR } sportsCar;


**strings**
- when using c-strings use #include <cctype>
- if c string contains non-digits, results may return:
    + results up to non-digit
    + 0
- itoa() does no bounds checking (character arrays)
- null terminator is '\0'

lol I failed this
