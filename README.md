# Target CPU Compiler

```
    cross-compiler-armv4eb
    cross-compiler-armv4tl
    cross-compiler-armv6l
    cross-compiler-i586
    cross-compiler-m68k
    cross-compiler-mips64
    cross-compiler-powerpc
    cross-compiler-sh2eb
    cross-compiler-sh4
    cross-compiler-x86\_64
    cross-compiler-armv4l
    cross-compiler-armv5l
    cross-compiler-i486
    cross-compiler-i686
    cross-compiler-mips
    cross-compiler-mipsel
    cross-compiler-powerpc-440fp
    cross-compiler-sh2elf
    cross-compiler-sparc
```

# How To Use

```
    [root@host] # docker pull r00kiter/cross-cpu-compile:latest
    [root@host] # docker run -itd r00kiter/cross-cpu-compile:latest sleep 1d
    [root@host] # docker exec -it [container-id] bash
    [root@container] # vim hello.c
         #include<stdio.h>
         int main() {
             printf("HELLO WORLD\n");
             return 0;
         }
    [root@container] # /root/compile_bins/cross-compiler-xxx/bin/xxx-gcc -o tt hello.c
```

# How To Build

```
    [root@host] # git clone https://github.com/rootkiter/cross-cpu-compile.git
    [root@host] # cd cross-cpu-compile
    [root@host] # docker build -t cross-cpu-compile .
    [root@host] # docker images
```

