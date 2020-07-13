# sequentialProcessor
For detailed documentation regarding this project, refer to the Sequential Processor PDF file. 

To gain a better understanding of computer architecture, I designed and implemented a sequential processor based arithmetic logic unit (ALU). 
The ALU is a combinational digital circuit that computes both arithmetic and logic operations on integer binary numbers. 

The ALU is a fundametal building block of the CPU; The control unit of the CPU directs the ALUs to perform a certain operation (based on instructions sent to the processor), with the result stored in registers. This is the crux of CPU operation, and why ALUs are so important. Current CPUs have multive ALUs and thus can carry multiple operations in parallel, driving performance. 

Sequential, or serial, processing executes instructions in the order that they were received, as opposed to parallel processing. The ALU developed herein utilizes the concept of the sequential processor, where the system executes operations in sequence using a multifunction ALU controlled by instruction memory. The system
also utilized a register with flip-flops to store the value. A clock signal is used to pace the operation of the flip-flops, with a frequency low enough to allow ALU outputs to be resolved. This employs sequential logic to control the ALU, as output state is stored in memory to be used as input in future operations.


