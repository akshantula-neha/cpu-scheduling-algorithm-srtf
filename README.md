# cpu-scheduling-algorithm-srtf
A Process Scheduler schedules different processes to be assigned to the CPU based on particular scheduling algorithms. These algorithms are either non-preemptive or preemptive. Non-preemptive algorithms are designed so that once a process enters the running state, it cannot be preempted until it completes its allotted time, whereas the preemptive scheduling is based on priority where a scheduler may preempt a low priority running process anytime when a high priority process enters into a ready state.

**Shortest Remaining Time First (SRTF)** is the preemptive version of **Shortest Job Next (SJN)** algorithm, where the processor is allocated to the job closest to completion. 

**Advantages**: 
SRTF algorithm makes the processing of the jobs faster than SJN algorithm, given it’s overhead charges are not counted. 

**Disadvantages**: 
The context switch is done a lot more times in SRTF than in SJN, and consumes CPU’s valuable time for processing. This adds up to it’s processing time and diminishes it’s advantage of fast processing.

