### HDLBits
Play with HDLBits

## Getting Started
1. Compliling (Logic Synthesis)  
HDL->Circuits
2. Simulation  
Circuit match/mismatch (ref)  
Waveform match/mismatch (timing diagram, ref)

## Verilog Language
# Basics
1. Wire: directional, continuous assignment. Assignment creates connections between wires. Wires are declared at the input/output
2. Inverter: bitwise-NOT(~), logical-NOT(!)
3. AND-Gate: bitwise-AND(&), logical-AND(&&)
4. XNOR-Gate: bitwise-XOR(^), no logical-XOR
5. Declaring wires: connect internal components together

# Vectors
1. type [upper:lower] vector_name
2. Implicit nets  
In Verilog, net-type signals can be implicitly created by an assign statement or by attaching something *undeclared* to a module port. Implicit nets are always one-bit wires.
`default_nettype none     // Disable implicit nets. Reduces some types of bugs. 
3. vector cannot be reversed directly, by bit assignment with concatenation to save a bit of coding.
4. Sign-extending, concatenation/replication
