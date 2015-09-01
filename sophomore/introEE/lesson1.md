*AC* is a sinusoidal wave. 110V / 60 Hz <- time variant

*DC* 12 V <- constant

**CPU**
- main task : perform computation
- datapath : collection of computational capabilities (load/store/add/subtract)
  - table of operations.
  - Boolean Functions
  - *basic building blocks*
    - Logic Gates & Flip-Flops
    - Register Transfer Level Components
- controller  : mechanism to arrange and apply.
  - table of methods.
  - Finite State Machine (necessary to write controller)
  - *basic building blocks*
    - Logic Gates & Flip-Flops
    - State Registers & Next State Registers
      - we will make a register later
- programmability
  - instruction set design (going to be on exam)
  - address modes

**Labs**
- Schematic Capture : design datapath circuits
- State Machine Editing : create controllers
- Goal: Design a Toy Processor with minimal instructions.
  - design a datapath/controller
  - implement it onto an FPGA board.
-

*we will only touch the concepts, do not need to delve deep*

**Information Representation**
1. Info e.g numbers, text, audio, video, etc
2. represent and store as binary digits {0,1}
  - 0 -> 0 - 0.8 V
  - 1 -> 2.5 - 5 V
  - computer looks at the ping/watev and determines whether its 0 or 1 depending on the voltage.


    1 bit = 2 combos
    2 bit = 2x2 combos = 4
    3 bit = 2x2x2 combos = 8

**number representation**
Each number is represented by a string of digits.
- Most significant bit (MSB) on the left
- Least significant bit (LSB) on the right


    1,234.56 = 1x10^3 + 2x10^2 + 3x10^1 + 4x10^0 + 5x10^-1 + 6x10^-2

**conversion**
- starting from *radix point* and going leftwards, bundle bits in groups of four and replace each group with digit.
- *if u put a `0x` before number, it means its hexidecimal*


    10 1001 1100.1010 1 (base 8) = 29C.A8 (base 16)
                ^radix point

- to convert decimal to binary, u keep dividing the number by 2, noting the remainder, until you reach a quotient of 0.

**subtraction of binary numbers**

|x|y|c|c+1|s=x+y+c|
|-|-|-|---|-------|
|0|0|0|  0|      0|
|0|0|1|  0|      1|
|0|1|0|  0|      1|
|0|1|1|  1|      0|
|1|0|0|  0|      1|
|1|0|1|  1|      0|
|1|1|0|  1|      0|
|1|1|1|  1|      1|

**addition of binary numbers**

**2's compliment**
1. invert digits (flip 1 and zeros)
2. add one (let remainders propogate)
- leading 0 means positive
- 
