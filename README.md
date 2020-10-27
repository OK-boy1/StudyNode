# studynode
个人学习笔记
@[TOC](汇编语言零基础入门学习)
#  基础知识
汇编语言是直接在硬件之上工作的编程语言，我们首先要了解硬件系统的结构，才能有效地应用汇编语言对其编程。
我们的原则是，以后用到的知识，以后再说。
## 1.1机器语言
机器语言是机器指令的集合。
机器指令展开来讲就是一台机器可以正确执行的命令。
## 1.2汇编的产生
汇编语言的主体是汇编指令。
汇编指令和机器指令的差别在于指令的表示方法上。
汇编指令是机器指令便于记忆的书写格式。

操作：寄存器BX的内容送到AX中
机器指令：1000 1001 1101 1000
汇编指令：mov ax，bx

（寄存器，简单地讲是CPU中可以存储数据的器件，一个CPU中有多个寄存器。AX是其中一个寄存器的代号，BX同理）

## 1.3汇编的组成
指令组成：
1.汇编指令：机器码的助记符，有对应的机器码。
2.伪指令：没有对应的机器码，由编译器执行，计算机并不执行。
3.其他符号：如+ － * /等，由编译器识别，没有对应的机器码。

汇编语言的核心是汇编指令，它决定了汇编语言的特性。


## 1.4存储器
CPU是计算机的核心部件，它控制整个计算机的运作并进行运算。
要想让一个CPU工作，就必须向它提供指令和数据。
指令和数据在存储器中存放，也就是我们平时所说的内存。
## 1.5指令和数据
指令和数据是应用上的概念。
在内存和磁盘上，指令和数据没有任何区别，都是二进制信息。
## 1.6存储单元
存储器别划分成若干个存储单元，每个存储单元从0开始顺序编号，如0~127。
电子计算机的最小信息单位是bit（比特），一个二进制位。
8bit = 1byte（字节）
1KB = 1024B 1MB = 1024KB 1GB = 1024MB 1TB = 1024GB
## 1.7CPU对存储器的读写
CPU进行数据的读写，必须和外部器件进行3类信息的交互：
- 存储单元的地址（地址信息）；
- 器件的选择，读或写的命令（控制信息）；
- 读或写的数据（数据信息）。

在计算机中专门有连接CPU和其他芯片的导线，通常称为总线。
总线从逻辑上分为3类：
- 地址总线
- 控制总线
- 数据总线
![  ](https://img-blog.csdnimg.cn/2020102719045813.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0VIb3JpemVu,size_16,color_FFFFFF,t_70#pic_center)

## 1.8地址总线
CPU是通过地址总线来指定存储单元的。
一个CPU有N根地址线，则可以说这个CPU的地址总线宽度为N。
这样的CPU最多可以寻找2的N次方个内存单元。
## 1.9数据总线
CPU与内存或其他器件之间的数据传送是通过数据总线来进行的。
数据总线的宽度决定了CPU和外界的数据传送速度。
## 1.10控制总线
CPU对外部器件的控制是通过控制总线来进行的。
控制总线的宽度决定了CPU对外部器件的控制能力。
## 1.11主板
主板，又叫主机板（mainboard）、系统板（systemboard）、或母板（motherboard）。它安装在机箱内，是微机最基本的也是最重要的部件之一。主板一般为矩形电路板，上面安装了组成计算机的主要电路系统，一般有BIOS芯片、I/O控制芯片、键盘和面板控制开关接口、指示灯插接件、扩充插槽、主板及插卡的直流电源供电接插件等元件。
## 1.12接口卡
能插入计算机、服务器或大型主机的板卡，通过光纤信道或SCSI把计算机连接到存储器或存储器网。主机总线适配器(Host Bus Adapter,HBA)是一个在服务器和存储装置间提供输入/输出(I/O)处理和物理连接的电路板或集成电路适配器。因为HBA减轻了主处理器在数据存储和检索任务的负担，它能够提高服务器的性能。一个HBA和与之相连的磁盘子系统有时一起被称作一个磁盘通道。
## 1.13各类存储器芯片
- 随机存储器
- 装有BIOS（Basic Input/Onput System,基本输入/输出系统）的ROM
- 接口卡上的RAM
## 1.14内存地址空间
内存地址空间的大小受CPU地址总线宽度的限制。
