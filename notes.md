# notes

## chapter 1

A major theme in computer systems is to provide abstract representations at different levels to hide the complexity of the actual implementations.

## chapter 2

The familiar decimal, or base-10, representation has been in use for over 1,000 years, having been developed in India, improved by Arab mathematicians in the 12th century, and brought to the West in the 13th century by the Italian mathematician Leonardo Pisano (ca. 1170 to ca. 1250), beher known as Fibonacci.

Using decimal notation is natural for 10-fingered humans, but binary values work better when building machines that store and process information.

Floating-point arithmetic is not associative due to the finite precision of the representation. For example, the C expression (3 .14+1e20)-1e20 will evaluate to 0.0 on most machines, while 3 .14+(1e20- 1e20) will evaluate to 3.14.

A single byte consists of 8 bits. In binary notation, its value ranges from 000000002 to 111111112. When viewed as a decimal integer, its value ranges from 010 to 25510. Neither notation is very convenient for *describing bit patterns*. Binary notation is too verbose, while with decimal notation it is tedious to convert to and from bit patterns. Instead, we write bit patterns as base-16, or hexadecimal numbers.

Every computer has a *word size*, indicatipg the nominal size of pointer data. Since a virtual address is encoded by such a word, the most important system parameter determined by the word size is the maximum size of the virtual address space.

## chapter 3

Computers execute machine code, sequences of bytes encoding the low-level operations that manipulate data, manage memory, read and write data on storage devices, and communicate over networks. A compiler generates machine code through a series of stages, based on the rules of the programming language, the instruction set of the target machine, and the conventions followed by the operating system.

The type checking provided by a compiler helps detect many program errors and makes sure we reference and manipulate data in consistent ways.

By reading this code, we can understand the optimization capabilities of the compiler and analyze the underlying inefficiencies in the code.

As described in Section 1.9.3, computer systems employ several different forms of abstraction, hiding details of an implementation through the use of a simpler abstrac\ model. Two of these are qpecially important for machine-level programming. First, the format and behavior of a machine-level program is defined by the instruction set architecture, or ISA, defining the processor state, the format of the instructions, and the effect each of these instructions will have on the state. ... Second, the memory addresses used by a machine-level program are virtual addresses, providing a memory model that appears to be a very large byte array.

The compiler does most of the work in the overall compilation sequence, transforming programs expressed in the relatively *abstract execution model* provided by C into the very elementary instructions that the processor executes.

**Being able to understand assembly code and how it relates to the original C code is a key step in understanqing how computers execute programs.**

Our goal in studying the examples shown in our presentation is to demonstrate how to examine assembly code and map it back to the constructs found in high-level programming languages. You will need to adapt these techniques to the style of code genarated by your particular ompiler.
