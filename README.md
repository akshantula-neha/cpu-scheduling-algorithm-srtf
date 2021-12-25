# cpu-scheduling-algorithm-srtf
A Process Scheduler schedules different processes to be assigned to the CPU based on particular scheduling algorithms. These algorithms are either non-preemptive or preemptive. Non-preemptive algorithms are designed so that once a process enters the running state, it cannot be preempted until it completes its allotted time, whereas the preemptive scheduling is based on priority where a scheduler may preempt a low priority running process anytime when a high priority process enters into a ready state.

**Shortest Remaining Time First (SRTF)** is the preemptive version of **Shortest Job Next (SJN)** algorithm, where the processor is allocated to the job closest to completion. 

**Algorithm**:

1- Traverse until all process gets completely executed.
      a) Find process with minimum remaining time at every single time lap.
   
      b) Reduce its time by 1.
   
      c) Check if its remaining time becomes 0 
   
      d) Increment the counter of process completion.
   
      e) Completion time of current process = current_time +1;
   
      f) Calculate waiting time for each completed process.
         wt[i]= Completion time - arrival_time-burst_time
   
      g)Increment time lap by one.
2- Find turnaround time,waiting time and response time.
   
**Advantages**: 
SRTF algorithm makes the processing of the jobs faster than SJN algorithm, given it’s overhead charges are not counted. 

**Disadvantages**: 
The context switch is done a lot more times in SRTF than in SJN, and consumes CPU’s valuable time for processing. This adds up to it’s processing time and diminishes it’s advantage of fast processing.

**Example:**
 Suppose we have the following 3 processes with process ID's P1, P2, and P3 and they arrive into the CPU in the following manner: 
 
![image](https://user-images.githubusercontent.com/90513459/147379209-862ac66f-bdc7-49ad-bf12-c78fe6eb62ad.png)

Gant Chart:

<img width="576" alt="GITHUB" src="https://user-images.githubusercontent.com/90513459/147107103-fd63a351-a999-4eec-9bab-540a2faababf.png">

Explanation:

At the 0th unit of the CPU, we have only process P1, so it gets executed for the 1-time unit.
At the 1st unit of the CPU, the Process P2 also arrives. Now, the P1 needs 7 more units more to be executed, and P2 needs only 2 units. So, P2 is executed by preempting P1.
P2 gets completed at time unit 3, and unit now no new process has arrived. So, after the completion of P2, again P1 is sent for execution.
Now, P1 has been executed for one unit only, and we have an arrival of new process P3 at time unit 4. Now, the P1 needs 6-time units more and P3 needs only 3-time units. So, P3 is executed by preempting P1.
P1 gets completed at time unit 7, and after that, we have the arrival of no other process. So again, P1 is sent for execution, and it gets completed at 13th unit.
SRJF algorithm

SRJF algorithm
![image](https://user-images.githubusercontent.com/90513459/147103796-b71e77c6-cbf8-481a-a794-cb1f7aad3ef2.png)


    Total Turn Around Time = 13 + 2 + 3
                = 18 milliseconds
    Average Turn Around Time= Total Turn Around Time / Total No. of Processes
                = 18 / 3
                = 6 milliseconds

    Total Waiting Time = 5 + 0 + 0
                = 5 milliseconds
    Average Waiting Time = Total Waiting Time / Total No. of Processes
                = 5 / 3
                = 1.67 milliseconds
                 
**OUTPUT**
![Screenshot (3)](https://user-images.githubusercontent.com/90513459/147379166-e991dbad-33d8-4539-a4f8-5ff84e7301a2.png)

