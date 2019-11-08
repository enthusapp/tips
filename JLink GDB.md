# GDB
##### monitor regs
##### monitor reset
##### stop continuing
https://stackoverflow.com/questions/3483163/how-do-i-halt-the-continuing-in-gdb

##### test memory
https://sourceware.org/gdb/current/onlinedocs/gdb/Memory.html
```
(gdb) x 0x10000000
0x1000020c:	0xffffffff
```

##### break
* reference: JLink manual
```
(gdb) file C:/temp/Blinky.elf
Reading symbols from C:/temp/Blinky.elf...done.
(gdb) target remote localhost:2331
Remote debugging using localhost:2331
0x00000000 in ?? ()
(gdb) monitor reset
Resetting target
(gdb) load
Loading section .isr_vector, size 0x188 lma 0x8000000
Loading section .text, size 0x568 lma 0x8000188
Loading section .init_array, size 0x8 lma 0x80006f0
Loading section .fini_array, size 0x4 lma 0x80006f8
Loading section .data, size 0x428 lma 0x80006fc
Start address 0x8000485, load size 2852
Transfer rate: 146 KB/sec, 570 bytes/write.
(gdb) break main
Breakpoint 1 at 0x800037a: file Src\main.c, line 38.
(gdb) continue
Continuing.
Breakpoint 1, main () at Src\main.c:38
38 Cnt = 0;
(gdb)
```

# JLink
##### JLink GDB Server Linux CLI
```
$ JLinkGDBServer -if SWD -device Cortex-M4
```
