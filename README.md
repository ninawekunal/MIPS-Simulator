# MIPS-5-Stage-Pipelined-Processor
5 Stage MIPS Processor in C++ with Pipelining implemented.
This is a cycle-accurate simulator for a 5-stage pipelined MIPS processor in C++. The simulator supports a subset of the MIPS instruction set and models the execution of each instruction with cycle accuracy. The MIPS program is provided to the simulator as a text file “imem.txt” file which is used to initialize the Instruction Memory. Each line of the file corresponds to a Byte stored in the Instruction Memory in binary format, with the first line at address 0, the next line at address 1 and so on. Four contiguous lines correspond to a whole instruction. Note that the words stored in memory are in “Big-Endian” format, meaning that the most significant byte is stored first. The Data Memory is initialized using the “dmem.txt” file. The format of the stored words is the same as the Instruction Memory. As with the instruction memory, the data memory addresses also begin at 0 and increment by one in each line.

MIPS pipeline has the following 5 stages:

1.Fetch (IF):fetches an instruction from instruction memory. Updates PC. 

2.Decode (ID/RF): reads from the register RF and generates control signals required in subsequent stages. In addition, branches are resolved in this stage by checking for the branch condition and computing the effective address. 

3.Execute (EX): performs an ALU operation. 

4.Memory (MEM): loads or stores a 32-bit word from data memory.

5.Writeback (WB): writes back data to the RF.
