## setup xv6-public runable in m1 mac

```
$ brew install qemu i686-elf-gcc
```

vim Makefile

```make
CFLAGS = -fno-pic -static -fno-builtin -fno-strict-aliasing -O2 -Wall -MD -ggdb -m32 -fno-omit-frame-pointer
```

그리고 qemu와 gcc 세팅을 해주어야한다. QEMU 부분의 주석을 풀고 TOOLPREFIX를 수정할 것이다.

```make
# If the makefile can't find QEMU, specify its path here
QEMU = qemu-system-i386

# Using native tools (e.g., on X86 Linux)
TOOLPREFIX = i686-elf-
```

이렇게 하면 끝. 빌드하고 실행해보자.

```bash
$ make clean
$ make
$ make qemu # GUI 윈도우가 뜸
$ make qemu-nox # 터미널에서 바로 실행
