# shellcode_example

a shecode example build on ubuntu 32bit.

write a sample shellcode, build it.
```sh
$ nasm -f elf helloworld.asm
$ ld helloworld.o
```

`runshellcode.c` will read a shekkcode.bin to a buffer, and run code from the buffer.

`$ gcc runshellcode.c -o runshellcode`

build your shellcode
```sh
$ cc -m32   -c -o shellcode.o shellcode.S
$ objcopy -S -O binary -j .text shellcode.o shellcode.bin
```

enjoy:
`$ ./runshellcode shellcode.bin`

---
# Reference

get more example from:
http://shell-storm.org/shellcode/files/shellcode-811.php
