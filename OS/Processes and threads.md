1. **New**
A program which is going to be picked up by the CPU into the main memory.
2. **Ready**
A newly created process directly enters the ready state, it waits for the CPU to be assigned. The OS picks the ready processes from the secondary memory and puts them in the main one.
Processes which are ready for execution and reside in the main memory are called **ready state processes**, there can be many of them.
3. **Running**
When a process has been chosen from the ready state by the OS. There will be as many running processes as many CPUs a PC has.
4. **Block or wait**
From the running state, a process can enter either the block or wait state depending on the scheduling algorithm or the behavior of the process.
When a process waits for a certain resource to be assigned or for user input, the OS puts it into either block/wait and assigns a new process to the CPU.
5. **Completion or termination**
When a process is finished, it enters the termination state. All the context of the process will be deleted, the process will be terminated by the OS.
6. **Suspend ready**
If a process from the ready state is moved back to the secondary memory due to lack of resources.
Or, when the memory's full and a higher priority process butts in, the other process will be suspended and will be thrown back to the secondary memory.
7. **Suspend wait**
If a process is currently waiting for resources it's better to move it to the secondary memory. They complete their execution when the main memory has space and their wait is finished.