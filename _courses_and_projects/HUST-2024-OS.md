---
title: "Operating System Practice"
collection: courses_and_projects
type: "Undergraduate course"
permalink: /teaching/HUST-2024-OS
venue: "Huazhong University of Science and Technology"
date: 2024-04-01
location: "Wuhan, Hubei"
---

The design goal of this experimental code is to give a set of operating system kernel development (operating system part) experiments driven by a given application on the RISC-V platform, as well as software and hardware co-design (system capability training part) experiments associated with the operating system. By completing part of the series of experiments on operating systems presented in this book, the reader will be able to develop an engineering understanding corresponding to the concepts learned in the Principles of Operating Systems course. Furthermore, by completing the series of experiments on system capability training given in this book, readers can establish a relatively complete understanding of the overall system composed of modern computer hardware (involving courses such as Principles of Computer Composition and Interface Technology) and underlying software (involving courses such as Principles of Operating Systems) from an engineering perspective.

以下为部分内容，其余请参见[仓库链接](https://github.com/ymx10086/HUST-2024-OS)

实验一 系统调用、异常和外部中断
=====

1.1	实验目的
===

本实验旨在深入了解操作系统的基本机制，特别是系统调用、异常和外部中断。通过进行相关实验，我们将能够实现以下目标：

1)	理解系统调用的概念及其在操作系统中的实现。

2)	掌握异常处理的原理，包括异常的产生、传递和处理机制。

3)	研究中断的机制，了解程序如何触发操作系统的响应。

通过完成以上目标，最终能够在操作系统的内部机制方面获得实际经验，提高对操作系统的整体理解水平。

1.2	实验内容
===

lab1_1 系统调用：

lab1_1实验在了解和掌握操作系统中系统调用机制的实现原理，进行完整的操作系统代码梳理后，具体思路如下：

1)	app的系统调用：从应用程序出发，发现user/app_helloworld.c文件中有两个函数调用：printu和exit。通过代码跟踪，我们发现这两个函数最终在user/user_lib.c中实现，而且它们最终都转换为对do_user_call函数的调用。

2)	系统调用的触发时机：深入研究do_user_call函数，发现它通过ecall指令来完成系统调用。在执行ecall指令之前，所有参数（do_user_call函数的8个参数）已经被加载到 RISC-V 机器的a0到a7寄存器中，这一步是编译器生成的代码自动完成的。

3)	系统调用和内核堆栈的处理：总的来说就是保存进程现场，切换到内核栈，执行S模式下的trap入口函数，如果系统调用是由用户程序触发的，即read_csr(scause)==CAUSE_USER_ECALL则执行handle_syscall()函数。最后，调用switch_to()函数返回当前进程。

4)	完成 lab1_1：将panic语句替换为对do_syscall()函数的调用，这样我们就能够通过系统调用完成特定的任务，而不会触发panic。

lab1_2 异常处理

lab1_2 异常处理的app中，（在用户U模式下执行的）应用企图执行RISC-V的特权指令csrw sscratch, 0。该指令会修改S模式的栈指针，如果允许该指令的执行，执行的结果可能会导致系统崩溃。因此，需要通过调用handle_illegal_instruction函数完成异常指令处理，阻止app_illegal_instruction的执行。具体思路如下：

1)	app的非法指令：从应用程序的角度出发，我们观察到user/app_illegal_instruction.c文件中的代码尝试执行一个在用户模式（U模式）下不允许运行的特权级指令：csrw sscratch, 0。
2)	非法指令触发异常：这个“异常事件”被识别为非法指令异常，对应的异常码是CAUSE_ILLEGAL_INSTRUCTION，其值为 02。

3)	异常交付：对于CAUSE_ILLEGAL_INSTRUCTION这类异常，我们通过代码追踪到m_start()函数执行delegate_traps()函数时的代理规则。查看相关代码发现，这类异常并没有交给 S 模式处理，而是由 M 模式处理。

4)	Trap入口：寻找M模式的trap处理入口，我们在 kernel/machine/mtrap_vector.S 文件中找到了mtrapvec汇编函数。在该函数中，调用了handle_mtrap()函数。

5)	完成lab1_2：将handle_mtrap()函数中对异常的处理逻辑从panic替换为调用handle_illegal_instruction()函数。

lab1_3 （外部）中断

lab1_3 （外部）中断完成PKE操作系统内核未完成的时钟中断处理过程，使得它能够完整地处理时钟中断。具体思路如下：

1)	时钟中断的初始化和触发：在 m_start 函数中新增了timerinit()函数，该函数设置下一次时钟中断触发的时间，并启用M模式中的时钟中断（MIE_MTIE位）。时钟中断的触发与lab2_1相似。不赘述。

2)	时钟中断处理：在 S 模式的smode_trap_handler函数中，检查scause寄存器的值，如果是由M模式传递上来的时钟中断动作（CAUSE_MTIMER_S_TRAP），则调用 handle_mtimer_trap() 函数进行处理。

3)	完成lab1_3：在handle_mtimer_trap()函数中，首先对全局变量g_ticks进行加一操作，用于记录时钟中断的次数。其次，清零SIP_SSIP位，以确保下次时钟中断时，M模式能够再次触发S模式的中断处理。这样，时钟中断的处理流程就得以完成。

1.3	实验调试及心得
===

在完成这三个操作系统实验的过程中，我深入理解了操作系统底层机制。通过分析应用程序和内核代码，我逐步追踪和理解了系统调用的执行流程，异常的触发机制以及时钟中断在 M 模式和 S 模式之间的处理流程。实践中，我自主完成了系统调用的实现，修改了异常处理逻辑，用实际的代码实现了对非法指令异常的处理。

这些实验不仅增强了我对操作系统原理的理解，还培养了我分析和解决底层问题的能力，为今后深入研究和应用操作系统奠定了坚实基础。
 