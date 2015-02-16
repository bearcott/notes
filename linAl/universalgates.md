#universal gates
- also known as *functionally complete*
- a binary gate takes 2 inputs
	- there are 4 possible input bits
	- 2^4 = 16 combinations of gates
- a **closed set of gates** happen when these gates cant make another gate not in the set.
	- e.g. the best way to determine a closed gate is to: (*this is called the fixpoint algorithm*)
		1. make a combo of three of them
		2. switch up the combo
		3. see if they can make other gates.
	- A set of gates is universal if and only if its smallest closed superset is the complete set.
- {NAND} and {NOR} are the only two single gate universal gates.