## **Course Objectives**
###### 1- Know the basic organization of OS
###### 2- Know the service an OS provides to users, processes and other systems
###### 3- Know the various ways of structuring an OS
###### 4- Know the notion of process an a thread
###### 5- Know CPU scheduling, which is the basis for multiprogrammed OS
###### 6- Know deadlocks
###### 7- Know a detailed description of various ways of organizing memory hardware.

## **Course Syllabus**
### **1- Introduction**

Main difference between computer organization and architecture.
- Computer architecture focus on  what are the components and how it's organized.
- Computer organization focus on how this components work internally.


#### 1.1- Computer System Structure
##### 1.1.1- 4 main Components
1- Hardware -> CPU, Memory, I/O devices
2- Operation System -> MAC, Windows, Linux
3- Application Programs -> Word, Chrome
4- Users -> Me

![Note Image](Pasted%20image%2020250427113220.png)

#### 1.2- What is an Operating System?
##### 1.2.1- Operating System is 
1- program that mange computer hardware
2- provides a basis for application programs
3- acts as an intermediary between User and Hardware

![[Pasted image 20250427113803.png]]

##### 1.2.2- Operating System Goals
1- Execute user programs
2- make the computer system convenient to use
3- Use the computer hardware in an efficient manner

#### 1.3- What Operating System do?
##### 1.3.1- OS **User View**
wants convenience, easy of use, good performance.
Shared computer must make all users happy.
User don\`t care about resource utilization.

##### 1.3.2- OS **System View**
A **resource allocator** -> make utilization for computer resources.
OS is a a resource allocator.
Manager of computer resources.
OS is a control program -> control executions of programs
##### 1.3.3- Kernel
A program that always run on computer.
The heart of the OS.


#### 1.4- Computer System Organization
##### 1.4.1- Modern general purpose Computer system
- memory
- CPU (1 or more)
- disk controller -> HDD, SSD
- USB controller -> mouse, keyboard, printer
- Graphics adapter -> monitor

![[Note Image](Pasted image 20250427145329.png)]

##### 1.4.2- Computer Startup
When you power up or reboot your PC, ***Bootstrap*** is loading.
Bootstrap stored in RAM or EPROM(firmware).
Initialize the whole system.
Loads Kernel. 

![[Note Image](Pasted image 20250427151025.png)]

##### 1.4.3- Interrupts
If hardware wants something from CPU, it will send an signals, by system bus. -> this is interrupt.
Software may trigger interrupt by executing a system call (monitor call).
each computer has it\`s own interrupt mechanism, but several functions are common.
when divides by zero in C, an exception occurs, this is similar to interrupt.
there are some exception that are stored somewhere within the OS, this place is interrupt vector, this place contains addresses of all service routine.
OS is an interrupt driven.
interrupt architecture must save the address of the interrupted instructions.
#### 1.5- Storage Structure
##### 1.5.1- Review
The basic unit of computer storage is the bit.
Byte = 8 bits.
OS deals with **Word**.
Word is 1 or more bytes.
KB = kilobyte -> 1024 bytes
MB = megabyte -> 1024^2 bytes
GB = gigabyte -> 1024^3 bytes
TB = terabyte -> 1024^4 bytes
PB = petabyte -> 1024^5  bytes

##### 1.5.2- Memory
**Main memory**
	RAM -> random access memory.
	it\`s Volatile -> when power off PC, everything gone.

**Secondary storage**
	HDD, SSD.
	Non volatile.
	SSD is faster than HDD.
	


**What is a register ?**
storge space that store one single operant
its in the prossceeor 
very fast (faster then cache)
expensive
volatile

**What is a cache ?**
storge space.
its in the prossceeor and motherboard
Fast (faster then RAM)
sheeper than registers
volatile

![[Note Image](Pasted%20image%2020250427153616.png)]

![[Note Image](Pasted%20image%2020250519000656.png)]



#### 1.6- Multiprocessing Architecture
Multiprocessor is more than 1 processor on the same system, to grow in use and importance.
it's also called parallel system.

##### 1.6.1- Advantages:
**1- increase throughput**: more processors -> more work in less time.
**2- Economy of scale**: multiprocessor systems less cost than multiple single processor system, Because they share peripherals, mass storage and power supply.
**3- Increased reliability**: you can rely on it.

##### 1.6.2- Types:
###### 1- Asymmetric multiprocessing
each processor assigned a specific task.
###### 2- Symmetric Multiprocessing
each processor preforms all tasks.

![[Note Image](Pasted%20image%2020250519002222.png)]

![[Note Image](Pasted%20image%2020250519002310.png)]

#### 1.7.1- Operating System Structure
##### 1.7.1.1- Multiprogramming (batch system) 
needed for efficiency.
it organizes jobs (code and data), so CPU has 1 to execute.
One job is selected and run via **job scheduling**.
when it has to wait, OS switch to another job.

![[Note Image]Pasted%20image%2020250519003015.png)]

Note: (A subset of total jobs in systems Kept in memory)

##### 1.7.1.2- Timesharing (Multi-tasking)
Logical extension -> CPU switch jobs -> user can interact with each job While it running.
##### 1.7.1.3- Goals:
1- **High** *response time* < 1 sec.
2- user has at least 1 executed program in memory ->Process.
3- many jobs ready to run at the same time -> CPU scheduling.
4- processes didn't fit ? -> swap them in and out to run.

Virtual memory allows execution of process that is not completely in memory.

#### 1.7.2- Operating System Operations
OS is an Interrupt driven.
Hardware interrupt by one of the devices.
Dual Mode operations protect OS and system components.
kernel mode = supervisor mode = system mode = privileged mode.
##### 1.7.2.1- Examples of software interrupt:
1- divides by zero.
2- Request for OS service
3- infinite looping 
and more.

##### 1.7.2.2- Kernel mode
A bit (mode bit) is added to hardware to indicates current mode (0->Kernel, 1-> user).
Some instructions  only executable in kernel mode.
System call changes mode to kernel.

![[Note Image](Pasted%20image%2020250519010258.png)]


##### Levels of storage:

![[Note Image](Pasted%20image%2020250519010335.png]]

#### 1.8- Protection and security
##### Protection
control access of processors and users to resources.
##### Security
defense system against attacks.

#### 1.9- Computing Environments
**portals** -> provides web accessibility to internal servers.
**Network computers** -> terminals that understand web based computing, used in workstations Where more security or easier maintenance is desired.
Mobile computers interconnect via Wireless networks.

Distinguish computing -> collection of separates, possibly heterogenies, system network together. 
Network OS provides features between system across network.

![[Note Image](Pasted%20image%2020250519011238.png)]
![[Note Image](Pasted%20image%2020250519011245.png)]

##### Virtualization
Allow OS to run applications within other Operating systems. 
**VMM** = Virtual Machine Manger -> provides virtualization services.

![[Note Image](Pasted%20image%2020250519011609.png)]

![[Note Image](Pasted%20image%2020250519011710.png)]

Cloud computing  -> Skip
public cloud -> skip
private cloud -> skip
Hyprid cloud -> skip

Skip
SAAS
PAAS
IAAS
### **2- Operating System Structures**
adeddcsdsf

### **3- Processes**
asfd

### **4- Threads**
afds

### **5- CPU Scheduling**
asfd

### **6- Process Synchronization**
asdf

### **7- Deadlocks**
asdf

### **8- Main Memory Management**
asdf
