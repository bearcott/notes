Table of common logical operations

|P|Q|P or Q|P and Q|P xor Q|P bicond Q|
|-|-|------|-------|-------|----------|
|0|0|0     |0      |0      |1         |
|0|1|1     |0      |1      |0         |
|1|0|1     |0      |1      |0         |
|1|1|1     |1      |0      |1         |

- OR - if one is true, then true (v)
- AND - both are true, then true (^)
- XOR - one is false one is true, then true ((+))
- Bicond - both are false or true, then true (<->)
- implied -  (->)

*if a logical expression is true for all values of its true table, then the expression is called a **tautology***

*if it is false for all is **contradiction***

*if it is conditionally true its **contingent***

|P|Q|PvQ|P->(PvQ)|
|-|-|---|--------|
|0|0|0  |1       |
|0|1|1  |1       |
|1|0|1  |1       |
|1|1|1  |1       |
