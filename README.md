Hello!

The following is my VCPU project I worked on to create a virtual Computer
This project was intended to be used to better learn how a computer not only runs from the base level,
but also how programs and compilers work.
The program also includes three registers, 
the GPREG for the data currently being manipulated, PCREG storing which line/instruction the compiler is on, and the IRREG storing the command of the current line.

The Assembler compiles the submitted file, converting entered commands into machine code based on the "codebook"
All command values in memory are stored in a 4 digit integer, with the first two values being the command, and final two being the operand, often memory location.
One limitation of the VCPU, is it only has 100 memory values, which is split between the commands of the submitted program, and the memory values utilized.
Below are the following commands.

    HALT  = 0   Ends the Program
    ADD   = 1   Adds the value at a a memory argument to the GPREG
    SUB   = 2   Subtracts the value at a memory argument to the GPREG
    MLT   = 3   Multiples the value at a memmory argument by the GPREG, then places value in the GPREG
    DIV   = 4   Divides the value at a memory argument by the GPREG, then places value in the GPREG
    ILOAD = 5   Loads a specific value into the GPREG
    LOAD  = 6   Loads a value at a memory location into the GPREG
    STOR  = 7   Stores the GPREG into memory
    READ  = 8   Reads user input
    WRITE = 9   Outputs the value at a specific memory location
    BR    = 10  Branch statement, return to line specificed
    BZ    = 11  Branch statement, if GPREG = 0, return to line specified
    BN    = 12  Brand statement, if GPREG != 0, return to lnie specified
    DUMP  = 13  Ouput all memory values

As a result of the project, you are able to produce basic assembly level programs.
