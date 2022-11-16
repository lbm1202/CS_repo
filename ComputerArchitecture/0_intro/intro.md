# intro

1. [Begin](##Begin)
2. [8 GreatIdea](##8-GreatIdea)
3. [Below Program](##Below-Program)
4. [Component of Computer](##Component-of-computer)
5. [Performance](##Performance)
6. [PowerWall](##PowerWall)
7. [Change in the future](##Change-in-the-future)
8. [Remarks](##Remarks)

>Written by Cho JungHee
junghee@zete.co.kr

***

## Begin

### The type of computer
1. Personal 
    - General use, various software
    - Various cost/performance
2. Server Computers
    - Network based
    - High capacity, performance, and reliability should be guaranteed
    - Therefore, usually expensive, large capacity, high performance.
    - Various from small server to building size
3. Super Computers
    - Used for complex calculations
    - Although it is high performance, it has cost problems such as very high price, power consumption, and maintenance cost, so it is used in limited places
4. Embeded Computers
    - Embedded, built-in, it is constituted as an element of the system
    - Required to be able to run from limited power, performance, memory and cost
    - In addition to aviation and medical systems, smartphones and tablets are also embedded systems

### *Computer Capacity unit
> 1 Byte == 8Bits
1 Kilobyte == 2<sup>10</sup>Bytes == 1024bits
1 Megabyte == 2<sup>20</sup>Bytes == 1024<sup>2</sup>bits
1 Gigabyte == 2<sup>30</sup>Bytes == 1024<sup>3</sup>bits
1 Terabyte == 2<sup>40</sup>Bytes == 1024<sup>4</sup>bits

### Summary
- How programs are translated into machine language 
    - How the hardware executes these instructions
- Hardware/Software Interface
- What determines program performance
    - How performance can be improved
- How will hardware designers advance performance
- What is parallel processing

***

## 8-GreatIdea
- It has contributed to the improvement of computer performance.
 
1. Designed for **Moore's Law**
2. Use **Abstraction** to simplify
3. Speed up **common**, **general** parts
4. Performance improvement through **Parallelism**
5. Performance improvement through **Pipelining**
5. Performance improvement through **Prediction**
6. **Memory system**
7. Improve reliability through **Redundancy**

***

## Below-Program
- Level of Program
    - Application Software
        - High Level Language like C, C++, Java
    - System Software
        - Compiler HLL to machine language
        - Operation Software
            - control I/O
            - manage memory
            - manage task & scheduling
    - Hardware
        - Processor, Memory, I/O

> High Level Language Code -> Assembly Language Code -> Hardware representation

***

## Component-of-computer
- All types of computers have the same elements
    - PC, server, or embedded..

1. User-interface device
    - Display, keyboard, mouse, ...
2. Storage
    - Hard disk, CD/DVD, flash, ...
3. Processor
    - Cpu, Gpu, ...

### Inside the Processor 
- Datapath: Execute data operation
- Control: control datapath order, memory, ...
- Cache memory : Small but high speed SRAM memory for quick data access

### Abstractions
- Technique that simplifies a complex problem so that it can be easily solved
 
- Abstractions help you to be more flexible.
    - Reduce low-level complexity
- Instruction set architecture (ISA, instruction set architecture)
    - ISA == Hardware/Software Interface
    - Software is made up of instructions
    - Hardware runs this(Software). Data is exchanged using instructions
- Application binary interface
    - ISA + system software interface
- develop
    - Basic details and interfaces

***

## Performance
- What is Performace
    - How to define "Performace"

### Response Time & Throughput
- Response Time : The time it takes to perform one task
- Throughput : How many tasks can be done per unit time
- What is Affected by Response Time and Throughput?
    > What if replace the processor with faster

    - Increase Response Time
    > What if more processor are worked

    - Response Time is same, Increase Throughput

### Relative Performance
- Performace = 1 / runtime
> A is N time faster than B
- N = Performace<sub>A</sub> / Performace<sub>B</sub> 
- = runtime<sub>B</sub> / runtime<sub>A</sub>  

### Measureing Execution Time
- Elapsed Time
    - Total response time from all aspects. 
        - Processing, I/O, OS overhead, idle time are all included
    - Used to determine system performance.
- CPU Time
    - Time taken to process a given task (purely time taken by the CPU)
        - Excluding time used for I/O or other operations
    - There are user CPU time and system CPU time.
    - Different programs have different effects on CPU and system performance.

### CPU Clocking
- Clock Peroid : Time of rising edge to rising edge
- Clock frequency : Cycle per second

### CPU Time
- CPU Time = CPU Clock Cycles * Clock Cycle Time = CPU Clock Cycles / Clock Rate

- How to improve Performace
    1. Decrease Clock Cycle
    2. Increase Clock Rate

### Instruction Count & Compiler
- Instruction Count?
    - determine by ISA & Compiler
- CPI (Average Cycles Per Instruction)
    - if instruction is different, CPI different too
    - mix instructions, calculate average CPI

### Summary
CPU Time = ( Instructions / Program ) * ( Clock Cycles / Instructions ) * ( Seconds / Clock Cycle )

***

## PowerWall
>\*In the computer architecture,"Wall" is used in two places,
Power and Memory.

Power = 0.5 * Capacity load * Voltage<sup>2</sup> * Frequency

***

## Change-in-the-future
>So far, performance has increased every year, but development has slowed down due to the limitations of semiconductors
Therefore, it was designed to improve performance through multi-core rather than single-core

### Amdahl's Law
- If you improve any part of your computer, you can see a proportional improvement in overall performance.

***

## Remarks


***