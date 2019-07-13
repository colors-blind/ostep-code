# Run code

mem.c

use `echo "0" > /proc/sys/kernel/randomize_va_space` to close address space randomization.

```bash
┌─[root@parrot]─[~]
└──╼ #echo "0" > /proc/sys/kernel/randomize_va_space
┌─[root@parrot]─[~]
└──╼ #more /proc/sys/kernel/randomize_va_space
0
```

compile code and run it

```bash
┌─[✗]─[root@parrot]─[/home/lovezx/Desktop/ostep-code/intro]
└──╼ #gcc -o mem mem.c -Wall -no-pie

┌─[✗]─[root@parrot]─[/home/lovezx/Desktop/ostep-code/intro]
└──╼ #./mem 1 & ./mem  2
[1] 14837
(14837) addr pointed to by p: 0x405260
(14838) addr pointed to by p: 0x405260
(14837) value of p: 2
(14838) value of p: 3
(14837) value of p: 3
```

## Todo:
What is address space randomization?

