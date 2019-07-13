# Run code

cpu.c

```
lovezx@parrot ~/D/o/intro> gcc cpu.c -o fishcpu

lovezx@parrot ~/D/o/intro> nohup ./fishcpu A &; nohup ./fishcpu B &; nohup ./fishcpu C &; nohup ./fishcpu D &;
nohup: ignoring input and appending output to 'nohup.out'
nohup: ignoring input and appending output to 'nohup.out'
nohup: ignoring input and appending output to 'nohup.out'
nohup: ignoring input and appending output to 'nohup.out'
```

ps to see processes

```
lovezx@parrot ~/D/o/intro> ps aux | grep fishcpu
lovezx   12288  103  0.0   2260   748 pts/3    R    18:56   0:19 ./fishcpu A
lovezx   12289  102  0.0   2260   748 pts/3    R    18:56   0:19 ./fishcpu B
lovezx   12290  102  0.0   2260   748 pts/3    R    18:56   0:19 ./fishcpu C
lovezx   12291  102  0.0   2260   748 pts/3    R    18:56   0:19 ./fishcpu D
lovezx   12339  0.0  0.0   4900   940 pts/3    S+   18:56   0:00 grep --color=auto fishcpu
```

pkill to kill process

```
lovezx@parrot ~/D/o/intro> pkill  fishcpu
fish: Job 4, 'nohup ./fishcpu D &' terminated by signal SIGTERM (Polite quit request)
fish: Job 2, 'nohup ./fishcpu B &' terminated by signal SIGTERM (Polite quit request)
lovezx@parrot ~/D/o/intro> 
fish: Job 3, 'nohup ./fishcpu C &' terminated by signal SIGTERM (Polite quit request)
fish: Job 1, 'nohup ./fishcpu A &' terminated by signal SIGTERM (Polite quit request)

```

pkill -9 kill process

```
lovezx@parrot ~/D/o/intro> pkill -9 fishcpu
fish: Job 4, 'nohup ./fishcpu D &' terminated by signal SIGKILL (Forced quit)
fish: Job 3, 'nohup ./fishcpu C &' terminated by signal SIGKILL (Forced quit)
fish: Job 2, 'nohup ./fishcpu B &' terminated by signal SIGKILL (Forced quit)
fish: Job 1, 'nohup ./fishcpu A &' terminated by signal SIGKILL (Forced quit)

```

