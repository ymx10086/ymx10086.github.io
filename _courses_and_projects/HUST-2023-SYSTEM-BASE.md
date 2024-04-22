---
title: "CSAPP Experiment"
collection: courses_and_projects
type: "Undergraduate course"
permalink: /teaching/HUST-2023-SYSTEM-BASE
venue: "Huazhong University of Science and Technology"
date: 2023-08-01
location: "Wuhan, Hubei"
---

The experiments of APP have the following in common: They have experienced the test of CMU classroom. The authors developed and refined these experiments in classrooms with 150 to 250 students over 10 years. The course is highly rated by students, who generally cite the experiments as the reason why they love the course. Automatic test and evaluation of drivers. Students write the solution in C and then link it to the C driver. The driver runs its solution, checks its correctness, and makes a quantitative evaluation of the solution. Students use this feedback to refine their answers.

以下为部分内容，其余请参见[仓库链接](https://github.com/ymx10086/HUST-2023-SYSTEM-BASE)

BOMB
=====

实验概述
===

本部分主要从实验的目的和意义、实验目标、实验要求和实验安排层面进行实验概述的介绍。

1. 实验目的和意义：本实验中，需要使用课程所学知识拆除一个“Binary Bombs”来增强对程序的机器级表示、汇编语言、调试器和逆向工程等方面原理与技能的掌握。

2. 实验目标：一个“Binary Bombs”（二进制炸弹，简称炸弹）是一个Linux可执行C程序，包含phase1~phase6共6个阶段。炸弹运行的每个阶段要求你输入一个特定的字符串，若你的输入符合程序预期的输入，该阶段的炸弹就被“拆除”，否则炸弹“爆炸”并打印输出 "BOOM!!!"字样。实验的目标是要拆除尽可能多的炸弹阶段。

3. 实验要求：（1）使用gdb调试器和objdump来反汇编炸弹的可执行文件;（2）通过gdb调试器进行单步调试，或者设置断点依次执行（3）理解每一汇编语言代码的行为或作用，尽可能设计出合适的字符串拆解炸弹。

4. 实验安排：尽可能在一次实验课程完成全部实验。

具体实验环境如下：

系统环境：Windows 10子系统WSL下安装的Ubuntu 20.04

GDB版本：GNU gdb (Ubuntu 12.1-0ubuntu1~22.04) 12.1

实验内容
===

本次实验主要为在linux环境下，使用gdb调试器和objdump来反汇编二进制炸弹的执行程序，根据调试和反汇编的结果破解包含phase1~phase6考察机器级语言程序的不同方面，难度逐级递增的六个阶段，另外还有一个隐藏阶段，但只有当在第4阶段的解之后附加一特定字符串后才会出现。本次实验破解了包括隐藏关卡的所有关卡。

缓冲区
=====

实验概述
===

本部分主要从实验的目的和意义、实验目标、实验要求和实验安排层面进行实验概述的介绍。

1. 实验目的和意义：本实验中，需要使用课程所学知识进行缓冲区的攻击操作，加深对IA-32函数调用规则和栈帧结构的理解。

2. 实验目标：对目标程序实施缓冲区溢出攻击（buffer overflow attacks）；通过造成缓冲区溢出来破坏目标程序的栈帧结构；继而执行一些原来程序中没有的行为

3. 实验要求：（1）使用gdb调试器和objdump来反汇编攻击代码的可执行文件;（2）通过gdb调试器进行单步调试，或者设置断点依次执行（3）理解每一汇编语言代码的行为或作用，尽可能设计出合适的字符串实现利用溢出区进行攻击的操作。

4. 实验安排：尽可能在一次实验课程完成全部实验。

具体实验环境如下：

系统环境：Windows 10子系统WSL下安装的Ubuntu 20.04

GDB版本：GNU gdb (Ubuntu 12.1-0ubuntu1~22.04) 12.1

实验内容
===

本实验需要对目标可执行程序“bufbomb”分别完成5个难度递增的缓冲区溢出攻击，5个难度依次为Smoke（level 0）、Fizz（level 1）、Bang（level 2）、Boom（level 3）和 Nitro（level 4）。
 