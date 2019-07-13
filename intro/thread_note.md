# Run cdoe

thread.c

```bash
lovezx@parrot ~/D/o/intro> gcc -o threads threads.c -Wall -pthread
lovezx@parrot ~/D/o/intro> ./threads 10
Initial value : 0
Final value   : 20
lovezx@parrot ~/D/o/intro> ./threads 1000
Initial value : 0
Final value   : 2000
lovezx@parrot ~/D/o/intro> ./threads 100000
Initial value : 0
Final value   : 132188
lovezx@parrot ~/D/o/intro> ./threads 10000000
Initial value : 0
Final value   : 11861798
```

`++` is not atomically executed.

