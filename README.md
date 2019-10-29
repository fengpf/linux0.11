Linux-0.11
==========

The old Linux kernel source ver 0.11 which has been tested under modern Linux,  Mac OSX and Windows.

## 1. Build on Linux

### 1.1. Linux Setup

* a linux distribution: debian , ubuntu and mint are recommended
* some tools: gcc gdb qemu
* a linux-0.11 hardware image file: hdc-0.11.img, please download it from http://www.oldlinux.org, or http://mirror.lzu.edu.cn/os/oldlinux.org/, ant put it in the root directory.
* Now, This version already support the Ubuntu 16.04, enjoy it.

### 1.2. hack linux-0.11
```bash
$ make help		// get help
$ make  		// compile
$ make start		// boot it on qemu
$ make debug		// debug it via qemu & gdb, you'd start gdb to connect it.
```
```gdb
$ gdb tools/system
(gdb) target remote :1234
(gdb) b main
(gdb) c
```

## 2. Build on Mac OS X

### 2.1. Mac OS X Setup

* install cross compiler gcc and binutils
* install qemu
* install gdb. you need download the gdb source and compile it to use gdb because port doesn't provide i386-elf-gdb, or you can use the pre-compiled gdb in the tools directory.
* a linux-0.11 hardware image file: hdc-0.11.img

```bash
$ sudo port install qemu
$ sudo port install i386-elf-binutils i386-elf-gcc
```

optional
```bash
$ wget ftp://ftp.gnu.org/gnu/gdb/gdb-7.4.tar.bz2
$ tar -xzvf gdb-7.4.tar.bz2
$ cd gdb-7.4
$ ./configure --target=i386-elf
$ make
```

### 2.2. hack linux-0.11
same as section 1.2


### 3. Build on Windows
todo...

### 操作系统之基础
https://mooc.study.163.com/learn/1000002004?tid=2402971010#/learn/content?type=detail&id=2403309701&cid=2403326984
L1 什么是操作系统
L2 开始揭开钢琴的盖子
L3 操作系统启动
L4 操作系统接口
L5 系统调用的实现
L6 操作系统概述
L7 操作系统历史
L8 我们的任务

### 操作系统之进程与线程
https://mooc.study.163.com/learn/1000002008?tid=2402970013#/learn/content?type=detail&id=2403307697&cid=2403327488
L9 多进程图像
L11 用户级线程
L12 核心级线程
L13 核心级线程实现实例
L14 CPU调度策略
L15 一个实际的schedule函数
L16 进程同步与信号量
L17 对信号量的临界区保护
L18 信号量的代码实现
L19 死锁处理

### 操作系统之内存管理
https://mooc.study.163.com/learn/1000003007?tid=2402971009#/learn/content?type=detail&id=2403307721&cid=2403326994
L20 内存使用与分段
L21 内存分区与分页
L22 段页结合的实际内存管理
L23 请求调页内存换入
L24 内存换出

### 操作系统之外设与文件系统
https://mooc.study.163.com/learn/1000002009?tid=2402969010#/learn/content
L25 IO与显示器
L26 键盘
L27 生磁盘的使用
L28 用文件使用磁盘
L29目录与文件系统
L30 目录解析代码实现

### 实验楼
https://www.shiyanlou.com/courses/115