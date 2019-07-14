# Question 4

We’ll now explore some of the other flags. One important flag is
-S, which determines how the system reacts when a process issues an I/O. With the flag set to SWITCH ON END, the system
will NOT switch to another process while one is doing I/O, instead waiting until the process is completely finished. What happens when you run the following two processes (-l 1:0,4:100
-c -S SWITCH ON END), one doing I/O and the other doing CPU
work?


```bash
lovezx@parrot ~/D/o/H/C/HW-CPU-Intro> python process-run.py -S SWITCH_ON_END -l 1:0,4:100 -c -p
Time     PID: 0     PID: 1        CPU        IOs 
  1      RUN:io      READY          1            
  2     WAITING      READY                     1 
  3     WAITING      READY                     1 
  4     WAITING      READY                     1 
  5     WAITING      READY                     1 
  6*       DONE    RUN:cpu          1            
  7        DONE    RUN:cpu          1            
  8        DONE    RUN:cpu          1            
  9        DONE    RUN:cpu          1            

Stats: Total Time 9
Stats: CPU Busy 5 (55.56%)
Stats: IO Busy  4 (44.44%)
```


