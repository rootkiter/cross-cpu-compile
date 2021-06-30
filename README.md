# Target CPU

```
    cross-compiler-armv4eb/bin/armv4eb-gcc
    cross-compiler-armv4tl/bin/armv4tl-gcc
    cross-compiler-armv4l/bin/armv4l-gcc
    cross-compiler-armv5l/bin/armv5l-gcc
    cross-compiler-armv6l/bin/armv6l-gcc

    cross-compiler-mipsel/bin/mipsel-gcc
    cross-compiler-mips/bin/mips-gcc
    cross-compiler-mips64/bin/mips64-gcc

    cross-compiler-m68k/bin/m68k-gcc

    cross-compiler-sparc/bin/sparc-gcc

    cross-compiler-powerpc/bin/powerpc-gcc
    cross-compiler-powerpc-440fp/bin/powerpc-440fp-gcc

    cross-compiler-sh4/bin/sh4-gcc
    cross-compiler-sh2eb/bin/sh2eb-gcc
    cross-compiler-sh2elf/bin/sh2elf-gcc

    cross-compiler-i486/bin/i486-gcc
    cross-compiler-i586/bin/i586-gcc
    cross-compiler-i686/bin/i686-gcc
    cross-compiler-x86_64/bin/x86_64-gcc
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

