# sequentialProcessor
For detailed documentation regarding this project, refer to the Sequential Processor PDF file. 

To gain a better understanding of computer architecture, I designed and implemented a sequential processor based arithmetic logic unit (ALU). 
The ALU is a combinational digital circuit that computes both arithmetic and logic operations on integer binary numbers. 

The ALU is a fundametal building block of the CPU; The control unit of the CPU directs the ALUs to perform a certain operation (based on instructions sent to the processor), with the result stored in registers. This is the crux of CPU operation, and why ALUs are so important. Current CPUs have multiple ALUs and thus can carry multiple operations in parallel, driving performance. 

Sequential, or serial, processing executes instructions in the order that they were received, as opposed to parallel processing. The ALU developed herein utilizes the concept of the sequential processor, where the system executes operations in sequence using a multifunction ALU controlled by instruction memory. This simple sequential processor also utilized a register with flip-flops to store the value. A clock signal is used to pace the operation of the flip-flops, with a frequency low enough to allow ALU outputs to be resolved. This employs sequential logic to control the ALU, as output state is stored in memory to be used as input in future operations.

The ALU designed is an 8-bit circuit, with operations on two 8-bit binary integers of: addition, subtraction, multiplication, and bitwise AND. To accomplish this, multiple circuits were implemented: 8-bit adder, 8-bit subtractor, 8-bit multiplier, 8-bit bitwise AND operator, 1-bit 4-to-1 multiplexer, 8-bit 4-to-1 multiplexer, and an 8-bit register. The first three circuits were used to perform said operations on two 8-bit binary integers. The bitwise AND operator compared the bits of two 8-bit binary integers in the same positions. The 1-bit 4-to-1 multiplexer was able to choose one of four 1-bit inputs as an output from a 2-bit selection input. Then, the 8-bit 4-to-1 multiplexer was an extension of the 1-bit 4-to-1 multiplexer, allowing four inputs and outputs to be 8-bit. The last subsystem was the 8-bit register which stored the output of the ALU after each operation. They were then combined to create the ALU. 

The ALU was implemented in Simulink, a MATLAB package used for both designing and simulating systems. Simulink was used to create the digital circuits, which were then modeled under various input conditions and then verified with the scope. Simulink's HDL Coder generated Verilog code from the model; This was used to test the system with Xilinx FPGA, on a ZedBoard platform. The various LEDs on the ZedBoard would light corresponding to the output value of the ALU. 

This project was useful, as a foundational component of processors was explored, then designed and implemented. Using digital logic, an 8-bit ALU was developed, demonstrating the power of combinational logic and sequential processing to perform arithemtic and logic manipulation. It is important to note that this same system can be scaled up, leading to the common 32-bit and 64-bit architecture that is commonplace today.    


