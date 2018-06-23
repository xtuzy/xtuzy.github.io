---
layout: post
title:  "数据结构之树"
date:   2018-06-22 23:14:54
categories: Notes
tags: C 数据结构 树
---
* content
{:toc}

包括树相关知识点和一些c语言知识



## C知识
1. 条件编译：有些程序在调试、兼容性、平台移植等情况下可能想要通过简单地设置一些参数就生成一个不同的软件，这时可以用条件编译，通过预编译指令设置编译条件，在不同的需求时编译不同的代码。
	- \#if—#elif—#else—#endif
```c	
			#if　条件1
				//条件1成立时编译
			#elif 条件2
				//条件2成立时编译
			#elif 条件n
				//条件n成立时编译
			#else
				//其他都不成立时编译
			#endif
```
	- \#ifdef—#else—#endif
```c
			#define MY_PRINT
			#ifdef MY_PRINT
				//之前定义了MY_PRINT时编译
			#else
				//未定义MY_PRINT时编译
			#endif
```
	- \#ifndef—#else—#endif
```c	
			//#define MY_PRINT
			#ifndef MY_PRINT
				//没有定义MY_PRINT时编译
			#else
				//定义MY_PRINT时编译
			#endif
```
	- \#if defined()—#elif defined()—#endif
```c	
			#define MY_PRINT_2
			#if defined(MY_PRINT_1)
				//定义MY_PRINT_1时编译
			#elif defined(MY_PRINT_2)
				//定义MY_PRINT_2时编译
			#endif
```
2. 	输入C语言 gets()和scanf()函数读取字符串的输入的区别(< stdio.h>)
	- gets可以接收空格；而scanf遇到空格、回车和Tab键都会认为输入结束，所有它不能接收空格
	- scanf("%s",字符数组名或指针); gets(字符数组名或指针)
	- scanf :当遇到回车，空格和tab键会自动在字符串后面添加`\0`，但是回车，空格和tab键仍会留在输入的缓冲区中。gets:可接受回车键之前输入的所有字符，并用`\n`替代 `\0`，回车键不会留在输入缓冲区中



