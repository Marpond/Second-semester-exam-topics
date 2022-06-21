## CPU
![](Pasted%20image%2020220621172434.png)
**Register**
Each register holds a particular purpose, they are a single, permanent storage location within the CPU.
A group of similar registers are often known as **register file**.

Most registers allow four types of operations:
1. Load values from other locations, deletes the current one.
2. Subtract or add a value from other locations, leaves the result.
3. Data can be shifted or rotated right or left by one or more bit.
4. The value of data can be tested. (0,+,-,capacity<)

**Control unit**
Controls and interprets the execution of instructions.

Control unit registers:
1. **Program counter register**
	- Holds the address of the current instruction.
2. **Instruction register**
	- Holds the actual instruction.
3. **Memory address register**
	- Holds the address of a memory location.
4. **Memory data register**
	- Holds a data value that is being stored to or retrieved from the memory location previously addressed by the MAR

The CU contains many **flags**. They are 1 bit registers, used to allow the computer to keep track of special conditions such as power failure, internal computer error, etc. Several flags are grouped into **status registers**.

**ALU**
Just like in LMC, this is where data is temporarily held and calculations are executed. In the CPU, the calculator equivalent is the **accumulator.** Modern CPUs have many accumulators, they're often known as:
- **General-purpose registers**
- **User-visible/Program-visible registers**

Along with holding data for the arithmetic operations and the results, these general-purpose registers also transfer data between different memory locations, and between I/O and memory.

**I/O interface**
Handles input and output data.

## Memory
Temporarily stores everything currently running on a device, after losing power it essentially forgets everything. 
Because of this, secondary storage is always needed, as we don't want to lose our documents after turning of our computers.
RAM, otherwise known as primary storage, is significantly faster than secondary storage, such as a HDD or SSD.

## Bus
They provide interconnection between various internal parts of the CPU, and between the CPU and memory, and so on. Buses can connect two components in a point-to-point config or may interconnect several modules in a multipoint config. The lines on buses carry signals that represent data, addresses, and control configs.