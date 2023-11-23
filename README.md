# XV Quiz (CSL 3030)

Welcome to the XV Quiz for CSL 3030 - Operating Systems!



## Instructions
- Answer the multiple-choice questions by selecting the correct option.
- For theoretical questions, provide concise and accurate explanations.
- Feel free to use this quiz for self-assessment or educational purposes.

## Multiple-Choice Questions

#### Question 1: Basics
1. What is XV6?
   - a. A programming language
   - b. A Unix-like operating system
   - c. A file system
   - d. An assembly language
   

#### Question 2: Architecture
2. XV6 is based on which earlier operating system?
   - a. Windows
   - b. Linux
   - c. BSD
   - d. DOS
   


#### Question 3: File System
3. Which file system is used in XV6?
   - a. FAT32
   - b. NTFS
   - c. ext4
   - d. simple
   - Answer

#### Question 4: System Calls
4. How are system calls implemented in XV6?
   - a. As functions in the C standard library
   - b. As interrupts
   - c. Through the command line
   - d. As external programs

#### Question 5: Processes
5. In XV6, what is the maximum number of processes that can run simultaneously?
   - a. 128
   - b. 256
   - c. 512
   - d. 1024

#### Question 6: Shell
6. What is the name of the shell used in XV6?
   - a. Bash
   - b. Zsh
   - c. Sh
   - d. Fish

#### Question 7: Scheduling
7. How does XV6 handle process scheduling?
   - a. Round-robin scheduling
   - b. Priority-based scheduling
   - c. First-Come-First-Serve (FCFS)
   - d. Random scheduling

#### Question 8: Memory Management
8. Which memory management technique is used in XV6?
   - a. Paging
   - b. Segmentation
   - c. Virtual Memory
   - d. None of the above

#### Question 9: Interrupts
9. How are interrupts handled in XV6?
   - a. Through polling
   - b. Using hardware interrupts
   - c. Using software interrupts
   - d. Both b and c

#### Question 10: Multithreading
10. Does XV6 support multithreading?
    - a. Yes
    - b. No

#### Bonus Question:
11. Who developed XV6?
    - a. Microsoft
    - b. Google
    - c. MIT
    - d. IBM

## Theoretical Questions

#### Question 12: Process States
12. Briefly explain the different states a process can be in within the XV6 operating system.

#### Question 13: File System Structure
13. Describe the structure of the file system in XV6. Include the key components and their roles.

#### Question 14: System Calls vs. Library Functions
14. Explain the difference between system calls and library functions in the context of XV6. Provide examples of each.

#### Question 15: Memory Paging
15. How does memory paging work in XV6? Discuss the benefits of using paging in memory management.

#### Question 16: Shell Commands
16. Name and briefly explain three essential shell commands in the XV6 operating system.

#### Question 17: Process Synchronization
17. Discuss the concept of process synchronization in XV6. Why is it essential, and what mechanisms are used to achieve it?

#### Question 18: Interrupt Handling
18. Explain the role of interrupts in the XV6 operating system. How are interrupts handled, and what is their significance in system operation?

#### Question 19: Virtual Memory
19. What is virtual memory, and how is it implemented in XV6? Discuss the advantages of using virtual memory.

#### Question 20: Boot Process
20. Outline the steps involved in the boot process of XV6. What happens from the moment the computer is powered on to when the XV6 kernel is loaded into memory?

## Answers
Please write your answers here

- (b)  A Unix-like operating system
- (c) BSD
- (d) Simple
- (b) Interrupts
- (a) 128
- (c) sh
- (a) Round-robin
- (a) Paging
- (d) both b and c
- (b) No
- (c) MIT

## Theoritical Answers

12. different states a process can be in within the XV6 operating system are as follows: 
      - - Ready
      - - Running
      - - Sleeping
      - - Zombie
      - - Unused

13. XV6 follows the hierarichal structure to store the files. It includes: 
      - - Directories: Directory to the file stored in the system
      - - InNodes: Stores the meta data about the files

14. System calls: These are the function calls made by the programs to access the kernel. Through these calls we can directly access the hardware resourcess (i.e. IO etc.). Ex: fork()

   Library functions: These are function calls which execute in the user mode and don't need admin permissions to execute. We can't directly access the hardware resources through these calls. Ex: any library function like printf()


15. In XV6, paging divides the process memory present in the secondary memory into pages and calls them into main memory when a page is requested by the processor. These pages when present in the RAM are called frames. This helps in the proper utilization of the RAM since it reduces the amount of unused memory in the RAM, allowing the machine to do multi processing. Also, this introduces the concept of virtual memory, which allows the users to load a process with memory size greater than the RAM size itself.

16. Three shell commands that I can remind are as follows: 
   - - 'ls': Gets all the files and directories present in a particular directory
   - - 'cd': Changes the root directory of the current shell
   - - 'mkdir': Creates a directory (folder)

17. Process synchronization in XV6 is implemented through locks which are similar to semaphores which we studied in the course. They lock the critical section when some process is accessing the resource. This is essential to prevent data inconsistencies in the process memory.

18. Interrupts are used to handle events that occur synchronously with respect tot the CPU. They are handled by the interrupt handler, which is a function that is called when an interrupt occurs. The interrupt handler then performs the necessary actions to handle the interrupt. Interrupts are important because they allow the CPU to handle events that occur asynchronously with respect to the CPU.

19. Virtual memory is a memory management technique that allows the operating system to use more memory than is physically available.

20. Following steps are performed: 
   - - computer is powered on.
   - - BIOS is loaded
   - - BIOS loads the loader
   - - loader loads the kernel
   - - kernel intializes the other programs requested by the user.
