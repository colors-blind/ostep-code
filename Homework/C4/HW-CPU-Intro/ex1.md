# Question 1

Run process-run.py with the following flags: -l 5:100,5:100.
What should the CPU utilization be (e.g., the percent of time the
CPU is in use?) Why do you know this? Use the -c and -p flags to
see if you were right.

100%

```bash
lovezx@parrot ~/D/o/H/C/HW-CPU-Intro> python process-run.py -l 5:100,5:100 -c -p
Time     PID: 0     PID: 1        CPU        IOs 
  1     RUN:cpu      READY          1            
  2     RUN:cpu      READY          1            
  3     RUN:cpu      READY          1            
  4     RUN:cpu      READY          1            
  5     RUN:cpu      READY          1            
  6        DONE    RUN:cpu          1            
  7        DONE    RUN:cpu          1            
  8        DONE    RUN:cpu          1            
  9        DONE    RUN:cpu          1            
 10        DONE    RUN:cpu          1            

Stats: Total Time 10
Stats: CPU Busy 10 (100.00%)
Stats: IO Busy  0 (0.00%)
```
