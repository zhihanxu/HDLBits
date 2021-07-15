# HDLBits
Play with HDLBits

## Getting Started
1. Compliling (Logic Synthesis)  
HDL->Circuits
2. Simulation  
Circuit match/mismatch (ref)  
Waveform match/mismatch (timing diagram, ref)

## Verilog Language
### Basics
1. Wire: directional, continuous assignment. Assignment creates connections between wires. Wires are declared at the input/output, 1bit default.
2. Inverter: bitwise-NOT(~), logical-NOT(!)
3. AND-Gate: bitwise-AND(&), logical-AND(&&)
4. OR-Gate: bitwise-OR(|), logical-OR(||)
5. XNOR-Gate: bitwise-XOR(^), no logical-XOR
6. Declaring wires: connect internal components together

### Vectors
1. type [upper:lower] vector_name
2. Implicit nets  
In Verilog, net-type signals can be implicitly created by an assign statement or by attaching something *undeclared* to a module port. Implicit nets are always one-bit wires.
`default_nettype none     // Disable implicit nets. Reduces some types of bugs. 
3. vector cannot be reversed directly, by bit assignment with concatenation to save a bit of coding.
4. Sign-extending, concatenation/replication

### Modules: Hierarchy
1. The hierarchy of modules is created by instantiating one module inside another.
2. Connect signals to module ports: by position/name
3. Full adder equations: sum = a^b^cin, cout = a&b|a&cin|b&cin
4. ripple carry adder -> delay of stage computing carry-out; carry-select adder: faster with a 2-to-1 mux.

### Procedures
1. Two types of always blocks: combinational: always @(*); clocked: always @(posedge clk)
2. Blocking vs. Non-Blocking assignment
3. Always if: 2-to-1 mux; conditional operator
4. Always case: 6-to-1 mux
5. Priority Encoder: outputs the position of the first 1 bit in the vector, using if or casez

### More Verilog Features
1. Conditional Ternary Operator: (()? a: ()? b: c))
2. Reduction operators: parity check; operate all bits of one vector
3. Long vector reversal: combinational for
4. Popcount: combinational for, if
5. *array instantiation/generate* for multiple instantiation such as Multiple bit full_adder, ripple carry adder


