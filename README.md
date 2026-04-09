
**COMPANY : CODTECH IT SOLUTIONS**
**NAME : MANAS KUMAR**
**INTERN ID : CTIS6553**
**DURATION : 8 WEEKS**
**MENTOR : NEELA SANTOSH**

**Design and Implementation of a 4-Stage Pipelined Processor**

In this task, I designed and implemented a 4-stage pipelined processor using Verilog and simulated it in Vivado. The main objective of this project was to understand the concept of pipelining in processor architecture and to implement a simple processor capable of executing basic instructions such as ADD, SUB, and LOAD.

The processor was divided into four stages: Instruction Fetch (IF), Instruction Decode (ID), Execute (EX), and Write Back (WB). Each stage performs a specific operation, and all stages operate simultaneously in a pipelined manner, which improves the overall throughput of the processor.

The design process began with the implementation of the Instruction Fetch (IF) stage. In this stage, I created a Program Counter (PC) module that generates the address of the instruction to be fetched. The PC increments on every clock cycle. This address is used by the Instruction Memory module to fetch the corresponding instruction. The fetched instruction is then stored in the IF/ID pipeline register, which acts as a buffer between the fetch and decode stages.

Next, I implemented the Instruction Decode (ID) stage. In this stage, the instruction stored in the IF/ID register is decoded to extract the opcode and operand fields such as source and destination registers. A Register File module was used to read the required operands based on the instruction fields. This stage is responsible for preparing the data required for execution. The decoded values and control signals are then passed to the next stage through the ID/EX pipeline register.

The third stage is the Execute (EX) stage, where the actual computation takes place. An Arithmetic Logic Unit (ALU) was designed to perform operations such as addition and subtraction based on the opcode. For the LOAD instruction, the ALU calculates the memory address. The output of the ALU is then forwarded to the next stage through the EX/WB pipeline register. Additionally, a Data Memory module was used to read data during LOAD operations.

Finally, the Write Back (WB) stage completes the instruction execution. In this stage, the result obtained from the ALU or Data Memory is written back into the Register File. This ensures that the result of one instruction can be used by subsequent instructions.

One of the most important aspects of this design was the use of pipeline registers (IF/ID, ID/EX, EX/WB). These registers enable the processor to execute multiple instructions simultaneously by holding intermediate data between stages. As a result, while one instruction is being executed, another can be decoded, and a third can be fetched, demonstrating true pipelined operation.

The design was simulated using a testbench in Vivado. The simulation results showed that multiple instructions were present in different stages of the pipeline at the same time. For example, while one instruction was in the Write Back stage, another was in the Execute stage, and a third was being decoded. This confirmed that the pipelining was functioning correctly.

In conclusion, this project successfully demonstrated the working of a 4-stage pipelined processor. The implementation improved my understanding of processor design, data flow, and parallel execution. The outcome of this project was a functional pipelined processor design along with simulation waveforms that clearly show the operation of each stage. This project also highlighted the importance of pipeline registers and stage separation in achieving efficient processor performance.

outcome:
<img width="1919" height="1071" alt="Image" src="https://github.com/user-attachments/assets/65d2017d-a916-4b74-bcbc-cc447ca12610" />
<img width="1919" height="1079" alt="Image" src="https://github.com/user-attachments/assets/5f0af3a1-7a30-4fa6-8580-3e4d6917eaa1" />
<img width="1919" height="1079" alt="Image" src="https://github.com/user-attachments/assets/bc19254f-35b3-45d1-8515-9c32ac83594c" />
<img width="1919" height="1079" alt="Image" src="https://github.com/user-attachments/assets/677c6bd3-748c-4323-a4ec-2fdf59678641" />
<img width="1919" height="1078" alt="Image" src="https://github.com/user-attachments/assets/9578607d-de8e-48ef-bf37-bdd1b9f72718" />
<img width="1919" height="1079" alt="Image" src="https://github.com/user-attachments/assets/14cf4942-9e36-4dd0-9890-4cf73e21eab3" />
<img width="1919" height="1075" alt="Image" src="https://github.com/user-attachments/assets/31e1c0e2-a77c-4cb9-8aab-74ceba54507c" />
<img width="1919" height="1074" alt="Image" src="https://github.com/user-attachments/assets/8ca7dd1e-032d-4974-88d9-8ad7f75e4e8d" />
