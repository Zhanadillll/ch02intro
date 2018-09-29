# ch02intro
Introduction to OS, Chapter 02

Read [Introduction to OS](http://pages.cs.wisc.edu/~remzi/OSTEP/intro.pdf) and answer the following review questions.

1. **What is an operating system? What does it do? 
   Operating system is body of software , which is responsible for making it easy to run programs , allowing programs to share memory ,
   enabling programs to interact with devices, and other fun stuff like that. It is in charge of making sure the system operates correctly    and efficiently in an easy-to-use manner
2. **What is virtualization?** 
   Virtualization -is primary way the OS does this is through a general technique .
   That is, the OS takes a physical resource  and transforms it into a more general,
   powerful, and easy-to-use virtual form of itself. Thus, we sometimes
   refer to the operating system as a virtual machine
3. **How does an OS provide access to its features? 
   OS provides some interfaces (APIs) that you can call. A typical OS, in fact, exports a few hundred system calls that are available to    applications. Because the OS provides these calls to run programs, access memory and devices, and other related actions, we also        sometimes say that the OS provides a standard library to applications
4. **What illusion does a virtualized CPU provide?**  
     It turns out that the operating system, with some help from the hardware,
     is in charge of this illusion, i.e., the illusion that the system has a
     very large number of virtual CPUs. Turning a single CPU  into a seemingly
     infinite number of CPUs and thus allowing many programs to seemingly run 
     at once is what we call virtualizing the CPU
    - **How does this affect the user experience?** 
      users interact with operating systems, with the help of this , certainly.
    - **How does this affect the developer experience?** your answer goes here 
    - **What if the CPU were not virtualized?** 
      Then , we can't emphasizes performance and runs directly on the processor whenever possible. The underlying physical resources are       used whenever possible and the virtualization layer runs instructions only as needed to make virtual machines operate as if they         were running directly on a physical machine
5. **What is a memory address?**
     if we want to read memory ,we should specify it to be able to access the data stored there
6. **What is memory virtualization?** 
     When we virtualizing memory. Each process accesses its own private virtual address space
     which the OS somehow maps onto the physical memory of the machine. A memory reference within
     one running program does not affect the address space of other processes;
     as far as the running program is concerned, it has physical
     memory all to itself. The reality, however, is that physical memory is
     a shared resource, managed by the operating system. .
    - **Why would we want this?** your answer goes here
     if we want to implement advantages , which mentioned above , we should use it 
8. **What happens if you write a C/C++ program that writes past the end of an array?**
    What happens really is undefined. When it happens in practice, the compiled program may end up writing those numbers to the memory       locations past array . This usually causes it to crash some of the time, but not always
    However, it can modify unrelated variables and have no visible effect. In some other instances, the writes may be optimized out and     the given compiled program only has the calls to an operator and that is without any unsafe operations. It is not really important       what exactly get to happen, the code will end up being invalid either way.
      - **Can this affect other programs?** your answer goes her
9. **What is a thread?** your answer goes here
    A thread is the smallest unit of processing that can be performed in an OS. In most modern operating systems, a thread exists within     a process - that is, a single process may contain multiple threads
10. **Why would we ever write a multi-threaded program?** 
    Because The main purpose of multithreading is to provide simultaneous execution of two or more parts of a program to maximum 
    utilize the CPU time. A multithreaded program contains two or more parts that can run concurrently. Each such part of a program          called thread. 
11. **What is atomicity?**
     Atomicity is a feature of databases systems dictating where a transaction must be all-or-nothing. 
     That is, the transaction must either fully happen, or not happen at all. It must not complete partially
    - **Is a C/C++ statement atomic?** your answer goes here 
    yes
    - **Is a Java statement atomic?** your answer goes here
    yes
    - **Is an assembler statement atomic?** your answer goes here 
    no
13. **What does persistence mean?** your answer goes here
    when power goes away or the system crashes, any data in memory
    is lost. Thus, we need hardware and software to be able to store data
    persistently; such storage is thus critical to any system as users care a
    great deal about their data
14. **How does OS hard drive virtualization differ from CPU & memory virtualization?** your answer goes here 
15. **How does running multiple programs at the same time increase CPU efficiency?** your answer goes here 
16. **What is multiprogramming?**
    Multiprogramming is a rudimentary form of parallel processing in which several programs are run at the same time on a uniprocessor.     Since there is only one processor, there can be no true simultaneous execution of different programs. Instead, the operating system     executes part of one program, then part of another, and so on. To the user it appears that all programs are executing at the same       time
