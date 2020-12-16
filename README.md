# xv6-Custom-Scheduling-Algorithm

The xv6 operating system has by default the round robin method.

In this project, I have created three different versions of xv6, each having one type of scheduling algorithm
1. FCFS - The older process has priority over the newer one
2. Priority - A user defined priority is used to decide which will get access to the CPU
3. Lottery - A probabilistic approach, where each process is given a set of tickets such that the one with more number of tickets is more likely to get the resources. Hence, a combination of round robin (each process gets the CPU for a while) and priority (the more important process will have more tickets)

Additional commands have been implemented whenever relevant:
* To get PID table: ps
* To change priority or number of tickets allocated: nice [pid] [new priority or count]
* To create long dummy processes to test scheduling: foo01 [number of processes] &;

To run the program use:
* make: Creates the xv6.iso file which will be the boot image
* make qemu-nox: Opens the xv6 OS in the terminal

For a better understanding of the mechanism, you may refer to the PPT
It has been implemented on Ubuntu 18.04 32-bit machine so make sure you have the correct qemu (different version exists for 64-bit)
