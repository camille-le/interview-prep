# Processes vs. Threads

## Processes
**_What's a program?_**
A program is an executable file that contains code, which is a set of processor instructions, that is stored as a file on disk.

**_What's a process?_** When the code in a program is loaded into memory and executed by the processor, it becomes a **process**. In addition, an active process includes the resources that a program needs to run, which are managed by the OS.

**_What are examples of resources needed for a process to run_?** Processor registers, program counters, stack pointers, memory pages assigned to the process for its heap and stack, etc.

![process.png](../img/process.png)

_**What's an important attribute of processes?**_ Each process has its own memory address space. Therefore, a single process cannot corrupt the memory space of another process. If one process malfunctions, other processes can keep running. 

One example of this is in Chrome where each tab is running as its own separate process. If one tab is not working, the other tabs are unaffected.

![process_mem_space.png](..%2Fimg%2Fprocess_mem_space.png)

## Threads
_**What is a thread?**_ A thread is a unit of execution within a process. A process has at least one thread, which is called the main thread. 

![thread.png](../img/thread.png)



What's the difference between a process and a thread?



### Sources
https://www.youtube.com/watch?v=4rLW7zg21gI&t=10s