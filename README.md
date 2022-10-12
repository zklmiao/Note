# 笔记

<!-- TOC  --> 
- [C](#c)                    
   - [变量](#变量)
   - [类型](#类型)
   - [作用域](#作用域)
   - [生命周期](#生命周期)
   - [类型转换](#类型转换)
   - [static](#static)
   - [sizeof](#sizeof)
   - [关键字 const extern volatile[扩展] register[扩展]](#关键字-const-extern-volatile扩展-register扩展)
   - [const #define](const-#define)
   - [运算符](#运算符)
   - [数组](#数组)
   - [一维数组和二维数组的转换](#一维数组和二维数组的转换)
   - [指针](#指针)
     - [指针概念](#指针概念)
     - [野指针](#野指针)
     - [内存越界](#内存越界)
     - [数组与指针](#数组与指针)
     - [二维指针](#二维指针)
     - [函数指针](#函数指针)
   - [函数与递归](#函数与递归)
   - [函数回调[see]](#函数回调see)
   - [malloc与动态内存分配](#malloc与动态内存分配)             
     - [内存溢出](#内存溢出)
     - [内存泄漏](#内存泄漏)
     - [内存对齐](#内存对齐)
     - [内存越界](#内存越界)
     - [malloc alloc realloc free new delete](#malloc-alloc-realloc-free-new-delete-new[]-delete[])
     - [内存池](#内存池)
   - [预编译与有参宏](#预编译与有参宏)
   - [结构体、共用体](#结构体共用体)
   - [结构体空洞](#结构体空洞)
   - [字符串操作](#字符串操作)        
     - [ strchar strlen strcpy strcat strcmp strstr atoi atof](#strchar-strlen-strcpy-strcat-strcmp-strstr-atoi-atof-strtol)
	 - [strlen实现](#strlen实现)
	 - [strcpy实现](#strcpy实现)
	 - [memcpy实现](#memcpy实现)
	 - [atoi实现](#atoi实现)
  - [编码规范](#编码规范)     
  - [数据结构](#数据结构)         
  - [线性表](#线性表)
      - [反转链表](#反转链表)
      - [快慢指针](#快慢指针)         
    - [队列](#队列)             
      - [链队列、循环队列、优先级队列](#链队列循环队列优先级队列)
   - [栈](#栈)             
      - [栈实现 栈应用:递归与非递归的转换](#栈实现-栈应用递归与非递归的转换)
    - [串操作](#串操作)             
      - [串基本操作、模式匹配、BF算法、KMP算法、最长公共前缀、最长公共子序列、验证回文串、最长回文子串(中心扩散法)](#串基本操作模式匹配bf算法kmp算法最长公共子序列)
    - [二叉树](#二叉树)             
      - [二叉树基本操作](#二叉树基本操作)
      - [BST](#bst)
      - [AVL](#avl)
      - [R-B tree](#r-b-tree)
      - [B+[扩展]](#b扩展)
      - [B-[扩展]](#b-扩展)
      - [B*[扩展]](#b扩展)
      - [替罪羊树](#替罪羊树)
      - [字典树](#字典树)
      - [树构建[扩展]](#树构建扩展)
    - [查找](#查找)             
      - [二分查找](#二分查找)
      - [线性查找-lineselect O(kn) [扩展]](#线性查找-lineselectO(kn)[扩展])
    - [索引](#索引)             
      - [hashTable](#hashtable)
    - [B树](#B-Tree)
      - [B- tree](#b-tree)
      - [B+ tree](#b+tree)
    - [八大排序[按考察重点排序]](#八大排序按考察重点排序)             
       - [Quick Sort](#quick-sort)
       - [Shell Sort](#shell-sort)
       - [Merge Sort](#merge-sort)
       - [Heap Sort](#heap-sort)
       - [Insert Sort](#insert-sort)
       - [Select Sort](#select-sort)
       - [Buble Sort](#buble-sort)
       - [Bucket Sort](#bucket-sort)
       - [Bitmap Sort](#bitmap-sort)
       - [Sort algorithem stablitiy](#sort-algorithem-stablitiy)
    - [时间复杂度](#时间复杂度)         
- [算法思想](#算法思想)             
   - [enum](#enum)             
   - [递归](#Recursion)             
   - [分而治之](#Divide-and-Conquer)             
   - [减而治之(剪枝)](#Decrease-and-Conquer(pruning))             
   - [DP(0-1pakge 8-queue Fibonacci[斐波那契] step[台阶问题-爬楼梯] 图DP-走到某处花费最小代价 最短编辑距离 找零钱)](#dp0-1pakge-8-queue-fibonacci斐波那契-step台阶问题-爬楼梯-图dp-走到某处花费最小代价-最短编辑距离-找零钱)             
   - [回溯 (DFS迷宫、DFS最短路、[DFS A-B 所有路径])](#Traceback-(DFS迷宫、DFS最短路、[DFS-A-B-所有路径]))             
   - [分支界限(分支定界、剪枝)](#Branch-and-Bound)             
   - [Greed(最小生成树[prime Kuskal]、Dijkstra最短路径)](#greed最小生成树prime-kuskaldijkstra最短路径)             
   - [概率算法(求PI)](#概率算法求pi)     
- [C++](#Cplusplus)         
   - [关键字](#关键字)             
     - [namespace](#namespace)             
     - [auto](#auto)             
     - [const](#const)             
     - [virtual](#virtual)             
     - [inline](#inline)             
     - [explicit](#explicit)             
     - [export[扩展]](#export扩展)             
     - [mutable[扩展]](#mutable扩展)         
   - [inline函数与有参宏](#inline函数与有参宏)
   - [指针与引用](#指针与引用)
   - [NULL与nullptr 区别](#null与nullptr-区别)
   - [const sizeof const与引用](#const-sizeof-const与引用)
   - [this指针](#this指针)
   - [封装(pubilc protect private)](#封装pubilc-protect-private)
   - [继承(多路径继承、虚继承[虚函数 纯虚函数 虚基类 虚析构的作用])](#继承多路径继承虚继承虚函数-纯虚函数-虚基类-虚析构的作用)
   - [虚基类表指针](#虚基类表指针)
   - [虚基类表](#虚基类表)
   - [什么是多态](#什么是多态)
     - [运行时多态](#运行时多态)
   - [友元与运算符重载](#友元与运算符重载)
   - [类拷贝(深拷贝、浅拷贝)](#类拷贝深拷贝浅拷贝)
   - [C++11智能指针](#C++11智能指针)
   - [C++四种类型转换(static_cast dynamic_cast const_cast reinpreter_cast)](#四种类型转换static_cast-dynamic_cast-const_cast-reinpreter_cast)
   - [class与struct区别](#class与struct区别)
   - [static与this指针](#static与this指针)
- [STL使用](#stl使用)
   - [STL主要有什么](#stl主要有什么)
   - [Vector 扩容](#vector-扩容)
   - [iterator erase(iterator) 后返回下一个](#iterator-eraseiterator-后返回下一个)
   - [map](#map)
   - [set](#set)
   - [map/set list 使用场景](#mapset-list-使用场景)
   - [STL源码[扩展]](#stl源码扩展)
   - [new malloc alloc](#new-malloc-alloc)
   - [delete free](#delete-free)
   - [string类实现](#string类实现)
   -  [什么是面向对象(OOP)](#什么是面向对象)
- [C++ 特性 lamda](#c-特性-lamda)         
- [C++ 编码规范(Google编码规范)[了解]](#c-编码规范google编码规范了解)         
- [Boost库[扩展]](#boost库扩展)     
- [Linux](#linux)         
   - [Linux开发环境](#linux开发环境)             
     - [常见命令](#常见命令)
     - [gcc编译器、动态链接库、静态链接](#gcc编译器动态链接库静态链接)             
	  - [gdb](#gdb)
      - [makefile](#makefile)
      - [shell编程](#shell编程)
      - [Valgrind[了解]](#valgrind了解)
  - [Linux系统编程](#linux系统编程)
  - [为什么使用IO多路复用?解决了什么问题?](#为什么使用IO多路复用?解决了什么问题?)             
    - [底层文件操作(不带缓冲的文件)、基本操作、printf、fprintf、sprintf](#底层文件操作不带缓冲的文件基本操作printffprintfsprintf)
  - [进程](#进程)             
    - [进程的基本概念、fork、exec、进程的五种状态切换、exit、shell的实现、守护进程](#进程的基本概念forkexec进程的五种状态切换exitshell的实现守护进程)             - [IPC](#ipc)
  - [IPC基本概念、管道、信号(进程间异步通信机制)、消息队列、内存共享、信号量(信号灯)](#ipc基本概念管道信号进程间异步通信机制消息队列内存共享信号量信号灯)
  - [多线程同步四种方式](#多线程同步四种方式)   
  - [死锁](#死锁)
  	- [进程死锁的原因](#进程死锁的原因)
	- [形成死锁的必要条件](#形成死锁的必要条件)
	- [死锁的处理](死锁的处理)      
  - [Linux socket编程](#linux-socket编程)
  - [socket基本操作](#socket基本操作)             
  - [select](#select)             
  - [epoll](#epoll)             
  - [线程池](#线程池)     
- [Windows](#windows)         
  - [Windows socket编程](#windows-socket编程)             
    - [IOCP](#iocp)
    - [select](#select-1)
  - [select与Epoll区别](#select与Epoll区别)
- [数据库](#数据库)         
  - [基本知识[待补充]](#基本知识待补充)             
    - [三大范式](#三大范式)
    - [SQL语句](#sql语句)
    - [MySQL基本用法](#mysql基本用法)
    - [索引机制-索引引擎[扩展]](#索引机制-索引引擎扩展)
  - [事务[扩展]](#事务扩展)     
- [Redis](#redis)         
  - [Redis 基本知识](#redis-基本知识)             
  - [redis和memcached有什么区别?](#redis和memcached有什么区别)             
  - [redis支持哪些数据结构](#redis支持哪些数据结构)             
  - [redis是怎么持久化的?](#redis是怎么持久化的)             
  - [redis同步机制?[扩展]](#redis同步机制扩展)             
  - [服务主从数据怎么交互的?[扩展]](#服务主从数据怎么交互的扩展)
  - [BloomFilter](#BloomFilter)             
  - [对方追问那如果突然机器掉电会怎样？[扩展]](#对方追问那如果突然机器掉电会怎样扩展)             
  - [redis缓存雪崩](#redis缓存雪崩)
  - [如何解决redis缓存雪崩](#如何解决redis缓存雪崩?)                        
  - [那你了解缓存穿透和击穿么，可以说说他们跟雪崩的区别么？](#那你了解缓存穿透和击穿么可以说说他们跟雪崩的区别么)             
  - [如何解决缓存穿透[业务逻辑上拦截、高级点:bloom filter]](#如何解决缓存穿透业务逻辑上拦截高级点bloom-filter)             
  - [如何解决缓存击穿](#如何解决缓存击穿)     
- [QT](#qt)         
  - [QT基本知识](#qt基本知识)             
  - [QT元对象系统](#qt元对象系统)             
  - [QT内存管理](#qt内存管理)             
  - [QT信号与槽](#qt信号与槽)             
  - [QT消息机制](#qt消息机制)             
  - [QT事件处理机制](#qt事件处理机制)             
  - [QT多线程](#qt多线程)             
  - [QT网络编程](#qt网络编程)             
  - [软件发布](#软件发布)     
- [设计模式](#设计模式)         
  - [设计模式基本知识](#设计模式基本知识)             
  - [单例模式](#单例模式)
	- [单例模式线程安全问题](#单例模式线程安全问题)
  - [工厂模式](#工厂模式)             
  - [观察者模式](#观察者模式)             
  - [git的使用](#git的使用)             
  - [UML](#uml)     
- [软件开发](#软件开发)         
  - [软件开发基本知识](#软件开发基本知识)             
  - [软件开发流程](#软件开发流程)             
  - [需求分析](#需求分析)            
  - [概要设计](#概要设计)           
  - [详细设计 coder拿到的](#详细设计-coder拿到的)             
  - [编码 coder](#编码-coder)             
  - [测试](#测试)     
- [计算机网络](#计算机网络)
  - [OSI七层模型与TCP/IP五层模型](#OSI七层模型与TCP/IP五层模型)
  - [三次握手](#三次握手)
    - [为什么是三次握手而不是两次?](#为什么是三次握手而不是两次?)
  - [四次挥手](#四次挥手)
    - [为什么是四次挥手](#为什么是四次挥手)
  - [TCP](#TCP)
    - [TCP和UDP区别](#TCP和UDP区别)
    - [TCP滑动窗口协议](#TCP滑动窗口协议)
    - [TCP握手以及每一次握手以及客户端和服务器处于那个状态](#TCP握手以及每一次握手客户端和服务器端处于哪个状态（11种状态）)
    - [TCP怎么保证可靠性（面向字节流，超时重传，应答机制，滑动窗口，拥塞控制，校验等）](#TCP怎么保证可靠性（面向字节流，超时重传，应答机制，滑动窗口，拥塞控制，校验等）？) 
    - [TCP/IP的分片粘包过程](#TCP/IP的分片粘包过程)
  - [UDP](#UDP)
- [操作系统](#操作系统) 
  - [大端机、小端机](#大端机小端机)
  - [大段字节序与小端字节序](#大段字节序与小端字节序)
  - [操作系统中进程调度策略有哪几种？](#操作系统中进程调度策略有哪几种？)
  - [进程和多线程](#进程和多线程)             
  - [进程的内存布局](#进程的内存布局)   
- [智力题](#智力题)  
<!-- /TOC  -->

## C
---
#### 变量
---
#### 类型
---
#### 作用域
---
#### 生命周期
> C源程序（.c）－>编译预处理(.i)－>编译(.s)－>优化程序－>汇编程序(.o)－>链接程序－>可执行文件(.exe)
---

#### 类型转换
---

#### static
static的作用主要有两种:
> 第一个作用是限定作用域；

> 第二个作用是设置变量存储域；

c语言中static的用法：

1、全局静态变量：

> 作用域：全局静态变量在声明他的文件之外是不可见的，准确地说是从定义之处开始，到文件结尾。

2、局部静态变量：

> 静态局部变量会覆盖静态全局变量

3、静态函数：

> 静态函数只能在本编译单元中使用
 

c++中static的用法：

1、类的静态成员：
```C++
　　class A{

　　private:

　　　　static int val;

　　};
```
> 　　在cpp中必须对他进行初始化，初始化时使用作用域运算符来标明他所属类，其属于该类的所有成员共有，只有一个拷贝；

　　2、类的静态成员函数：
```C++
　　class A{

　　private:

　　　　static int func(int x);

　　};
```
> 　　 实现的时候也不需要static的修饰.类的静态函数不能访问类的私有成员，只能访问类的静态成员，不需要类的实例即可调用；静态成员函数可以继承和覆盖，但无法是虚函数；

　　3、只在cpp内有效的全局变量：

> 　　在cpp文件的全局范围内声明：
```C++
　　static int val = 0；
```
> 　　这个变量的含义是该cpp内有效，但是其他的cpp文件不能访问这个变量；如果有两个cpp文件声明了同名的全局静态变量，那么他们实际上是独立的两个变量；

　　4、只在cpp内有效的全局函数：

> 　　函数的实现使用static修饰，那么这个函数只可在本cpp内使用，不会同其他cpp中的同名函数引起冲突；

#### sizeof
> 　sizeof是一种单目操作符,它并不是函数。sizeof操作符以字节形式给出了其操作数的存储大小。

#### 关键字 extern volatile[扩展] register[扩展]
extern
>  extern 表明变量或者函数是定义在其他其他文件中的,在文件中其他位置或者其他文件中寻找这个变量或者函数.全局函数默认前面带有extern.

volatile
> volatile提醒编译器它后面所定义的变量随时都有可能改变，因此编译后的程序每次需要存储或读取这个变量的时候，都会直接从变量地址中读取数据。如果没有volatile关键字，则编译器可能优化读取和存储，可能暂时使用寄存器中的值，如果这个变量由别的程序更新了的话，将出现不一致的现象.

register
> register：这个关键字请求编译器尽可能的将变量存在CPU内部寄存器中，而不是通过内存寻址访问，以提高效率.如果定义了很多register变量，可能会超过CPU的寄存器个数.

#### const #define
> 以 #define pi 3.1415 为例#define 是一个编译时概念 在程序编译时会将定义的宏在代码中替换,它生命周期止于编译期,存在于代码段.程序中被替换的内容是一个常数.
---

>const修饰的数据类型是指常类型，常类型的变量或对象的值是不能被更新的. const 常量存在于程序的数据段中,在栈区分配空间,const常量是一个运行时概念.const常量是有数据类型的,宏常量是没有数据类型的.编译器会对const常量进行类型安全检查.
---

#### 运算符
---

#### 数组
```C
	char a[] = "abc";
	char b[] = {'a','b','c'}; //这样写 b中不会有结束符'\0'
	// sizeof 二者占用内存 同为 4;

	// 字符串长度 a 3 b 3 二者等长.
	// 但是 b[]字符数组没有结束符'\0' 在末尾填充.故用strlen() 无法确定 字符数组b[]长度,因为所得的值是不可靠的.
	int c, d;
	c = strlen(a); 
	d = strlen(b);  // strlen所返回的值不可靠.
```
---

#### 一维数组和二维数组的转换

字符数组、字符串

字符串:
> 双引号引起的都是字符串.

> 字符串以'\0'结尾,没有则不是.[!C中的强制规定]

字符数组:
> 没有'\0'.

但是 char *str = "hello,world"; =(等价于)=> char str1[] = {'h','e','l','l','o','w','o','r','l','d','\0'};

---

### 指针
#### 指针概念
> CPU 通过内存寻址对存储在内存中的某个指定数据对象的地址进行定位,指针是保存这个地址的变量.指针是一种保存变量地址的变量。
#### 野指针
> 指针变量中的值是非法内存地址，进而形成野指针.

野指针由来

> 1、局部指针变量没有初始化

>  2、指针所指向的变量在指针之前被销毁

>  3、使用已经释放过的指针

>  4、进行了错误指针运算

>  5、进行了错误的强制类型转换

二级指针

> 指向指针的指针.

指针、堆、栈、指针形参

```C
// case 1:
void Getmemory(char *str)
{
	char p[] = "hello,world";
	str = p; // 此处 p[] 存储域在栈中,函数调用结束,则在栈中内存将会被释放.
}
char *str = NULL;
GetMemory(str);
printf("%s",str); // 打印仍为空

// case 2:
void Getmemory(char *p)
{
	// 此处编译器会为参数p 创建拷贝副本 _p 即在编译中会有 _p = p;
	p = (char*)malloc(100);// 实际上是由 _p 来执行此语句 _p = (char*)malloc(100); p 中的内容仍为修改.因此p中的内容并没有改变.

	strcpy(p,"hello,world");
}
char *str = NULL;
GetMemory(str);
printf("%s",str); // 打印仍为空

对于上面两问题的修改:
// 二级指针
void Getmemory(char **p)
{
	*p = (char*)malloc(100);
	strcpy(*p,"hello,world");
}
char *str = NULL;
GetMemory(&str); // 传递的是指针的地址
printf("%s",str); 

// 方法二 返回指针 即开辟空间的地址
char* Getmemory(size_t n)
{
	char* p  = (char*)malloc(n); // !!! 但需要注意,返回的值不能是指向栈内存中的内容.
	strcpy(p,"hello,world");
	return p;
}
char *str = NULL;
str = GetMemory(100);
printf("%s",str); 

// case 3:
char* Getmemory()
{
	char p[] = "hello,world";
	return p;
}
char *str = NULL;
str = GetMemory();
printf("%s",str); // 输出垃圾数据 栈中的程序已消亡 返回的是栈中的数据

对于case 3:修改
char* Getmemory()
{
	char *p = "hello,world"; // 指向常量区中的内容
	return p;
}
char *str = NULL;
str = GetMemory();
printf("%s",str);


```


---

#### 数组与指针
---
#### 二维指针
---
#### 函数指针
什么是函数指针
> 函数在编译后都是存储在内存中，并且每个函数都有一个入口地址,函数指针就是通过指向这个函数的入口，从而调用这个函数.
---
函数指针与指针函数
> 函数指针是一个指向函数的指针，而指针函数只是说明他是一个返回值为指针的函数.
---
#### 函数与递归 
---
#### 函数回调[see]
什么是回调函数
> 简单来说就是将一个存有函数入口地址的函数指针作为参数传入另一个函数中,当满足某条件是即调用该指针指向的函数响应该条件所触发的事件,即为函数回调(callback).

### malloc与动态内存分配

#### 内存泄漏
> 申请的空间没有正确释放.
---

#### 内存溢出
> 调用栈溢出（即stackoverflow），虽然这种情况可以看成是栈内存不足的一种体现.内存空间装不下.
----

#### 内存对齐
> 结构体作为成员:如果一个结构里有某些结构体成员,则结构体成员要从其内部"最宽基本类型成员"的整数倍地址开始存储.(struct a里存有struct b,b里有char,int ,double等元素,那b应该从8的整数倍开始存储.).
---

#### 内存越界
> 内存访问越界.
---

#### malloc alloc realloc free new delete new[] delete[]
malloc
> void* malloc(size_t n) 返回 (void*) 未确定类型的指针,指向一段可用内存的起始地址.分配大小至少为参数 n 所指定的字节数.malloc只管分配内存，不管对其进行初始化，得到的一片新内存中，其值将是随机的.

new 
> new返回指定类型的指针，并且可以自动计算所需要的大小.

alloc
> 返回值同malloc (void*) 只是参数不同alloc(size_t n, size_t size),返回大小为n*size 字节的内存块起始地址.

realloc
> void* realloc(void* p, size_t size) 修改指针p 指向的内存块的大小,并返回修改后的内存块的起始地址.若size(修改后的内存块大小)小于传入指针所指内存块大小则分配失败,返回NULL. realloc(void* p, size_t size) 不对新申请的内存块进行初始化.

free
> void free(void *ptr) 释放之前调用 calloc、malloc、realloc 所分配的内存空间.

delete 
> 在针对简单的基本数据类型，使用delete也可以回收 new[] 分配的一组对象的内存空间，因为：基本的数据类型对象没有析构函数，并且new 在分配内存时会记录分配的空间大小，则delete时能正确释放内存，无需调用析构函数释放其余指针.因此两种方式均可.
---

#### 内存池
---

#### 预编译与有参宏
```C++
#define cube(x) ((x)(x)(x))
```
> 宏可以带参数 在C++ 中可用inline替代


   指令         用途

    #           空指令，无任何效果
    #include    包含一个源代码文件
    #define     定义宏
    #undef      取消已定义的宏
    #if         如果给定条件为真，则编译下面代码
    #ifdef      如果宏已经定义，则编译下面代码
    #ifndef     如果宏没有定义，则编译下面代码
    #elif       如果前面的#if给定条件不为真，当前条件为真，则编译下面代码，其实就是else if的简写
    #endif      结束一个#if……#else条件编译块
---

#### 结构体、共用体
结构体位域
```C
struct node
{
    char ch : 4 // 指定占用 4字节
    char ch1 : 4
    int num;
};
typedef struct node node;
node a;
sizeof(a) = 4+4+4 = 12;
```
---

#### 结构体空洞
> 内存对齐机制,占用空间大的成员前的较小的成员由于内存对齐原因同样会占用与占用内存较大成员的内存,在这块内存中没有存有其他成员进行内存补齐,这一现象称为结构体空洞.
>
>解决办法,后根预留成员函数做内存补齐,或者书写时严格按照内存占用从小到大的顺序编写.

如下面的例子：
```C++
struct node
{
    char ch;
    int num;
    char ch1;
};
```
> 正常分析输出结果应该为1+4+1=6;可输出结果为12；因为第一个char系统为它分配4个字节，可它只用得到一个字节，剩余3个闲置。

> 第二个是int型，占四个字节，前面只剩3个字节，它不会填充到前面空间中，系统会重新分配给它四个字节，这四个字节被填满了。
> 
> 然后到第二个char，它不会填充到第一个char型剩余的3个字节中，而是系统又为它分配4个字节存储空间，还是会有3个字节闲置。最后总共占用12个字节。
---

### 字符串操作
#### strchar strlen strcpy strcat strcmp strstr atoi atof strtol
strchar
> char* strchar(const char* string, int target) 在字符串中找target(中间会将(int)target转换为(char)target)并返回该target在该串位置的指针.若没有匹配到则返回NULL.

strstr
> char* strstr(const char* str, const char* substr) 在str总找到substr子串,若找到则返回该子串第一次出现位置的首字母的指针,找不到返回NULL.

strtol
> long strtol( const char *str, char       **str_end, int base/*10:10进制 8:8进制 16:16进制*/);
---
#### strlen实现
```C
// v1
size_t MyStrlen(const char* str)
{
	int i = 0;
	while(*str != '\0')
	{
		*str++;
		i++;
	}
	return i;
}

// v2 不用局部变量 全局变量 实现strlen
//Tip: 懂v1 迭代写法就懂 v2 递归写法.
size_t MyStrlen_v2(const char* str)
{
	return *str == '\0' ? 0 : MyStrlen((++str)) + 1;
}
```

#### strcpy实现
> Tip: 标准库 string.h 提供的 strcpy(char* dest, const char* src) 有潜在的栈溢出风险,当dest 指向内存块大小不足以容纳,src时,字符串拷贝会出现栈溢出.

```C
	char str[2] = "a";
	const char *str1 = "def";
	strcpy(str, str1);
```

```C
//v1 自动避免栈溢出 dest指向的内存块能拷就拷多少.
void MyStrcpy(char* dest, const char* src)
{
	if (!dest || !src) return;
	while ((*dest != '\0') && (*src != '\0'))
	{
		*(dest++) = *(src++);
	}
}
//v2 自动避免栈溢出 但用户可以指定拷贝长度,在指定的长度小于等于 dest指向的内存块的大小 时成立.
void MyStrcpy(char* dest, const char* src, size_t n)
{
	if (!dest || !src) return;
	int i = 1;
	while ((*dest != '\0') && (*src != '\0')&&i<=n)
	{
		*(dest++) = *(src++);
		i++;
	}
}

// v3 处理内存重叠
void MyStrcpy(char* dest, const char* src, size_t n)
{
	if (!dest || !src) return;
	int i = 0;
	if(dest < src)
	{
		while ((*dest != '\0') && (*src != '\0')&&i<n)
		{
			*(dest++) = *(src++);
			i++;
		}
	}
	else
	{
		dest += (n-1);
		src += (n-1);
		while((*dest != '\0') && (*src != '\0')&&i<n)
		{
			*(dest--) = *(src--);
			i++;
		}
	}
}
```

#### memcpy实现
```C
// string.h中的实现,不处理内存重叠,若有内存重叠情况交由memmove()处理;
void* Memcpy(void* dest, const void* src,size_t count)
{
	if (!dest || !src || !count) return NULL;
	char* cdest = (char*)dest;
	const char* csrc = (char*)src;
	int i = 1;
	while ((cdest != '\0') && (csrc != '\0') && i <= count)
	{
		*(cdest++) = *(csrc++);
		i++;
	}
	return dest;
}


// 处理内存重叠
void* Mymemcpy(void* dest, const void* src, size_t count)
{
	if (!dest || !src || !count) return NULL;
	char* cdest = (char*)dest;
	char* csrc = (char*)src;

	int i = 0;
	if (dest < src) //高位地址向地位地址拷贝
	{
		while ((cdest != '\0') && (csrc != '\0') && i < count)
		{
			*(cdest++) = *(csrc++);
			i++;
		}
	}
	else
	{
		cdest += (count - 1);
		csrc += (count - 1);
		while (i < count)
		{
			*(cdest--) = *(csrc--);
			i++;
		}
	}
	return dest;
}
```

#### atoi实现
> ``` #include <cctype> ```

> ```int isspace(int ch);```

> ```int isdigit(int ch);```
```C
// #include <cctype>
//int isspace(int ch); 如果字符是空白字符，返回非零值，否则返回零。
//int isdigit(int ch); 若字符为数字则为非零值，否则为零。
int MyAtol(const char* str)
{
	if (!str)
	{
		std::cout << "str is null!" << std::endl;
		return 0;
	}

	while (isspace(*str)) str++;
	
	int Inter =	1;
	if (*(str++) == '-')
		Inter = -1;

	int val = 0;
	while (isdigit(*str))
	{
		val = val * 10 + (*str - '0');
		str++;
	}
	
	return Inter * val;
}
```
## 编码规范
## 数据结构
#### 输出二进制
```C
void DEC_2_binSystem(size_t n, size_t x)
{
	std::vector<int> ans;
	while (n != 1)
	{
		//printf("%d", (n % 2));
		ans.push_back((n % 2));
		n /= 2;
	}
	ans.push_back((n % 2));
	//printf("%d \n", (n % 2));
	std::reverse(ans.begin(), ans.end());
	for (int i : ans)
		std::cout << i;
	std::cout << std::endl;
}
```

#### 输出x进制
```C
void DEC_2_xSystem(size_t n,size_t x)
{

}
```
#### 字符统计
#### 括号匹配
### 线性表
#### 数组、单链表（各种操作插⼊、删除、遍历、排序、查找、创建、销毁、逆序） 、循环链表、双向链表
```C++
//单向链表结构体
struct OneWayNode;
struct OneWayNode
{
  int data;
  OneWayNode* next;
};
typedef struct OneWayNode Node_s;

// 双向链表结构体
struct TwoWayNode;
struct TwoWayNode
{
  int data;
  TwoWayNode* pre;
  TwoWayNode* next;
};
typedef struct TwoWayNode Node_d;
```
---
#### 反转链表
>Tip1: 解法一空间换时间

>Tip2: 解法二三指针原地算法.
```C++
Node* listRserver(Node *header)
{
	Node* cur; 
	Node* pre;
	Node* t;
	cur = header->next;
	pre = header;
	t = cur->next;
	while (t)
	{
		
		cur->next = pre;
		pre = cur;
		cur = t;
		t = cur->next;
		if (!t)
		{
			cur->next = pre;
			pre = cur;
			cur = t;
		}
	}
	header->next = NULL;
	return pre;
}

Node* listRserver_v2(Node *header)
{
	Node* cur; 
	Node* pre;
	Node* t;
	cur = header->next;
	pre = header;
	t = cur->next;
	while (cur)
	{
		
		cur->next = pre;
		pre = cur;
		cur = t;
		if(t)
			t = cur->next;
	}
	header->next = NULL;
	return pre;
}
```

#### 快慢指针
判断链表是否有环
> 快慢指针,不停转圈圈,总有一天会相遇.

判断两链表是否有交叉
> 空间换时间,备忘录法,地址哈希.若有相同点则能查询到.

### 队列
#### 链队列、循环队列、优先级队列
---

### 栈
#### 栈实现 栈应用:递归与非递归的转换
---

### 串操作
#### 串基本操作、模式匹配、BF算法(暴力算法-逐一匹配)、KMP算法、最长公共子序列[题目待补充]

> 回文数:atoi() Tip: printf("%i\n", atoi(" -123junk"));

最大子段和
```C++
int getMaxSubSum(const int *arr,int lenght)
{
  int tsum = 0;
  int maxsum = 0;
  for(int i = 0;i < lenght;i++)
  {
      tsum+=arr[i];
      tsum > maxsum ? (maxsum = tsum) : (tsum = 0);
  }
  return maxsum;
}
```
最长公共前缀
> Tip: O(n) 同时匹配.

---
回文串
> Tip.回文串只有两种模式:

> "aabaa"--单数回文串 

>"aabbaa" --双数回文串

验证回文串
```C++
// 对半比较
bool isPalindromic(const char* str1)
{
  std::string str = str1;
  int lenght = str.length();
  if(NULL == str1) return false;
  if(1 == lenght) return true;

  // [0 1 0] = 3 --单数回文串
  // [0 1 1 0] = 4 --双数回文串 
  if(lenght%2) // 单数回文串
  {
    int l = 0;
    int r = lenght - 1;
    while(l!=r)
    {
      if(str[l]!=str[r])
        return false;
      l++;
      r--;
    }
  }
  else // 双数回文串
  {
    int l = 0;
    int r = lenght - 1;
    while(r != (lenght/2))
    {
      if(str[l]!=str[r])
        return false;
      l++;
      r--;
    }
  }
  return true;
}
```

可构造最长回文串长度

>Tip:Greed、统计

> 输入:"abccccdd"

> 输出:7

> 解释:我们可以构造的最长的回文串是"dccaccd", 它的长度是 7。

>现在我们考虑一下可以构成回文串的两种情况：

> ①字符出现次数为双数的组合[统计重复出现的字符] 2n+2n+2n+... = m(2n)

> ②字符出现次数为双数的组合+一个只出现一次的字符[统计只出现一次的字符、重复出现的字符] (2n-1)+2n+2n+2n+...

> ① [aa bb cc] -> abccba [aa bb cc dd] -> dabccbad : lenght = m(2n)

> ② [aa bb cc e] -> abcecba [aa bb cc dd eee] -> dabceeecbad m(2n)+k

```C++
int getMax_Pli_Str_Length(const char* str)
{
  // 统计
  std::map<char, int>kmap;
  for(size_t i = 0;i < strlen(str);i++)
    kmap.insert({str[i],0});

  for(size_t i = 0;i < strlen(str);i++)
    kmap[str[i]]++;
  
  // Greed
  int single = 0;
  int sum = 0;
  for(auto& iter : kmap)
  {
    if(!(iter.second%2))
    	sum+=iter.second;
    else
      single > iter.second ? (single) : (single = iter.second);
//    std::cout<<iter.first<<"-"<<iter.second<<std::endl;
  }
   return (sum+=single); 
}
```

最长回文子串
> Tip1:中心扩散法O(n^2) Greed

```C++
// 确定中心 左右扩散 验证是否是回文串
void getMax_Pli_Substr(const char* str)
{
  int lenght = strlen(str);
  if(1 == lenght || NULL == str)
    return;
  //处理单数回文串,插入# 使单数回文串变为双数回文串.
  // zabbal -> z#a#b[#]b#a#l 双数回文子串[length = 11]
  // zabcbal -> z#a#b#[c]#b#a#l 单数回文子串[length = 13]
  // 经过这样处理无论是单数回文子串还是双数回文子串都可用对称处理.
  	std::string tstr;
  	for(size_t i = 0;i < lenght - 1;i++)
  	{
    	tstr+=str[i];
    	tstr+="#";
  	}
  	tstr+=str[lenght-1];
	std::cout<<tstr<<std::endl;
	
	std::string pilstr;
	std::string res;
	std::string s;
	// 定中心 
	for(int flage = 0; flage < tstr.length()-1;flage++)
	{
		int l,r;	
		// 左右扩散 取子串
		l = flage;
		r = flage;
		if(l)l--;
		if(r<tstr.length())r++;			
		for(int i = l;i<=r;i++)
			s+=tstr[i];
	
		std::cout<<flage<<" "<<s<<std::endl;

		while(true)
		{
			if(isPalindromic(s.c_str()))
			{
				if(s.length()>=pilstr.length())
					pilstr=s;
				if(l)l--;
				if(r<tstr.length())r++;
					s.clear();			
				for(int i = l;i<=r;i++)
					s+=tstr[i];
			}
			else 
				break;
		}
//		std::cout<<flage<<" "<<s<<std::endl;
		s.clear(); 
	}
		
	std::string t;
	for(int i = 0; i < pilstr.length(); i++)
	{
		t=pilstr[i];
		if(t.compare("#"))
			res+=pilstr[i];
			t.clear();
	}
	std::cout<<res<<std::endl;
}
```

> Tip2:manacher 算法O(n) DP

---

LCS
> BF O(n^3)

> DP On(n^2) 打表 滚动数组


解法一 二维表DP
```C++
void LCS_V1(const char* str1,const char* str2)
{
  	if(!str1||!str2)
		  return ;
	
	int length = (strlen(str1)*strlen(str2));

	int *record = new int[length];
	for(int n = 0; n < length;n++)
		record[n] = 0;
		
	std::string s1, s2;
	if(strlen(str1) > strlen(str2))
	{
		// 去较长的字符串为行 
		s1 = str2; //模式 // target
		s2 = str1; //串  // 被查找的串 source text	}
	else
	{
		s1 = str1;
		s2 = str2;
	}

    for(size_t j = 0; j < s2.length();j++)
    record[j] = (s1[0] == s2[j]);
  	for(size_t i = 1;i < s1.length();i++)
	{
		for(size_t j = 0; j < s2.length();j++)
    	{
    		if(j)
    			record[i*s2.length()+j] = (s1[i] == s2[j])+record[(i-1)*s2.length()+j-1];
    		else
    			record[i*s2.length()+j] = (s1[i] == s2[j]);
    	}
  	}
  
    int rank = 0;
    int t = record[0];
    for(int i = 0;i < length;i++)
  	{
  		t >= record[i] ? :(t = record[i],rank = i);
  	}
  	std::string res;
  	while(t)
  		res+=s1[t--];
  	for(int l = res.length()-1;l>-1;l--)
  	std::cout<<res[l];
  	delete []record;
}

```

解法二 备忘录DP
```C++
void LCS_V2(const char* str1,const char* str2)
{
  	if(!str1||!str2)
		  return ;
		
	std::string s1, s2,tstr,res;
	if(strlen(str1) > strlen(str2))
	{
		// 去较长的字符串为行 
		s1 = str2; //模式 // target
		s2 = str1; //串  // 被查找的串 source text
	}
	else
	{
		s1 = str1;
		s2 = str2;
	}
	for(int i = 0;i < s1.length();i++)
	{
		for(int j = 0;j < s2.length();j++)
		{
			if(s1[i] == s2[j])
			{
				while(i<s1.length()&&j<s2.length())
				{
					if(s1[i] == s2[j])
					{
						tstr+=s1[i];
						i++;
						j++;
					}
					else
						break;
					
				}
				if(res.length() < tstr.length())
					res=tstr;
				tstr.clear();
			}
		}
	}
	std::cout<<res<<std::endl;	
}
```


解法三 滚动数组DP
```C++
// maxlenght(str1,str2) ,str1,str2 二者中最长者为串,另一个则为模式,开辟数组长度为(max(str1.length,str2.length))*2
void LCS_V3(const char* str1,const char* str2)
{
  	if(!str1||!str2)
		return ;
	
	int length = std::max(strlen(str1),strlen(str2))*2;

	int *record = new int[length];
	for(int n = 0; n < length;n++)
		record[n] = 0;
		
	std::string s1, s2;
	if(strlen(str1) > strlen(str2))
	{
		s1 = str2; //模式 
		s2 = str1; //串 
	}
	else
	{
		s1 = str1;
		s2 = str2;
	}
	
	for(size_t j = 0; j < s2.length();j++)
		record[j] = ((s1[0] == s2[j]));
	
	
	for(size_t i = 0;i < s1.length();i++)
	{
		for(size_t j = 0; j < s2.length();j++)
		{
      // 滚动 数组
			if(!(i%2))
			{
        //...........递推
			}
			else
			{
        //..........递推
			}
			
		}
		std::cout<<std::endl;
	}
	
//	for(int n = 0; n < length;n++)
//		std::cout<<record[n]<<" ";
//	std::cout<<std::endl;
	
	delete []record;
}
```

####　删除所有子串

### 二叉树
#### 二叉树基本操作
```C++
// 叶子节点结构体
struct Node;
struct Node
{
  const char* data;
  Node* lc;
  Node* rc;
};
typedef struct Node TreeNode;
```

DLR
```C++
// 递归
void DLR(TreeNode* root)
{
  if(root->data)
    printf("%s ",root->data);
  if(root->l)
    DLR(root->l);
  if(root->r)
    DLR(root->r);
}

// 非递归,栈迭代写法
void DLR_iteration(TreeNode* root)
{
	if (!root) return;
	std::stack<TreeNode*> NodeStack;
	NodeStack.push(root);
	TreeNode* t = NULL;
	printf("%s ", NodeStack.top()->data);
	NodeStack.pop();
	// 迭代左子树 进栈顺序 右->左->中 出栈顺序 中->左->右
	if (root->lc)
		NodeStack.push(root->lc);
	while (!NodeStack.empty())
	{
		printf("%s ", NodeStack.top()->data);
		t = NodeStack.top();
		NodeStack.pop();
		if (t->rc)
			NodeStack.push(t->rc);
		if (t->lc)
			NodeStack.push(t->lc);
	}

	// 迭代右子树 进栈顺序 右->左->中 出栈顺序 中->左->右
	if (root->rc)
		NodeStack.push(root->rc);
	while (!NodeStack.empty())
	{
		printf("%s ", NodeStack.top()->data);
		t = NodeStack.top();
		NodeStack.pop();
		if (t->rc)
			NodeStack.push(t->rc);
		if (t->lc)
			NodeStack.push(t->lc);
	}
	std::cout << std::endl;
}

void DLR_iteration_v2(TreeNode* root)
{
	std::vector<const char*> ans;
	if (root == NULL) return ;
	std::stack<TreeNode*> s;
	s.push(root);

	while (!s.empty()) {
		TreeNode* top = s.top();
		s.pop();
		ans.push_back(top->data);
		if (top->rc) s.push(top->rc);
		if (top->lc) s.push(top->lc);
	}

	for (auto i : ans)
		std::cout << i << " ";
}

```
LDR
```C++
void LDR(TreeNode* root)
{ 
  if(root->l)
    LDR(root->l);
  if(root->data)
    printf("%d",root->data);
  if(root->r)
    LDR(root->r);
}

// 非递归 栈迭代写法
void LDR_iteration(TreeNode* root)
{
	if (!root) return;
	std::stack<TreeNode*> NodeStack;

	while (root || !NodeStack.empty())
	{
		// 将左节点全部压到栈中 
		while (root)
		{
			NodeStack.push(root);
			root = root->lc;
		}

// 1 最左 左节点出栈 / 栈顶元素出栈
		printf("%s ", NodeStack.top()->data);
		root = NodeStack.top();
		NodeStack.pop();
// 2 压入第二左节点(最左节点的父节点)的 右节点
// 若无,重复 1,2 步骤
		root = root->rc;	
	}
}

void LDR_iteration_v2(TreeNode* root)
{
	if (!root) return;
	std::stack<TreeNode*> NodeStack;
	std::vector<const char*> ans;//存储结果集

	while (root || !NodeStack.empty())
	{
		while (root)//当前节点不能为空
		{
			NodeStack.push(root);//压栈
			root = root->lc;//继续往左走
		}

		//printf("%s ", NodeStack.top()->data);
		ans.push_back(NodeStack.top()->data);
		root = NodeStack.top();//此时左子树已经走到尽头,返回栈顶元素
		NodeStack.pop();//弹栈
		root = root->rc;//往右走一步

	}
	for (auto i : ans)
		std::cout << i << " ";
}
```

LRD
```C++
void LRD(TreeNode* root)
{
  if(root->l)
    LRD(root->l);
  if(root->r)
    LRD(root->r);
  if(root->data)
    printf("%s ",root->data);
}

// 非递归 栈迭代写法
void LRD_iteration(TreeNode* root)
{
	std::vector<const char*> ans;
	if (root == NULL) return;
	std::stack<TreeNode*> s;
	s.push(root);

	while (!s.empty()) {
		TreeNode* top = s.top();
		s.pop();
		ans.push_back(top->data);
		if (top->lc) s.push(top->lc);
		if (top->rc) s.push(top->rc);
	}
	
	std::reverse(ans.begin(), ans.end());
	for (auto i : ans)
		std::cout << i << " ";
}
```

二叉树一般BFS
```C++
void BFS_Nomal(TreeNode* root)
{
  std::queue<TreeNode*> NodeQueue;
  if(root)
  NodeQueue.push(root);
  while(!NodeQueue.empty())
  {
    printf("%d ",NodeQueue.front()->data);
    if(NodeQueue.front()->l)
      NodeQueue.push(NodeQueue.front()->l);
    if(NodeQueue.front()->r)
      NodeQueue.push(NodeQueue.front()->r);
    NodeQueue.pop();
  }
}
```

二叉树按层BFS
```C++
void BFS_layer(TreeNode* root)
{
  if(!root) returnl;
  std::stack<TreeNode*> PrintStack;
  std::queue<TreeNode*> GetQueue;
  PrintStack.push(root);
  while(!PrintStack.empty())
  {
    int i = 1;
    printf("Layer %d:",i);
    while(PrintStak.empty())
    {
      printf(" %d ",PrintStack.top());
        if(PrintStack.top()->r)
          GetQueue.push(PrintStack.top()->r);
        if(PrintStack.top()->l)
          GetQueue.push(PrintStack.top()->l);
      PrintStack.pop();
    }
    printf("\n");
    while(!GetQueue.empty())
    {
      PrintStack.push(GetQueue.front());
      GetQueue.pop();
    }
  }
}
```

二叉树按层BFS扩展:
打印树的最右孩子
```C++

```

---

#### BST
> BST（二叉搜索树）查找思想也是二分思想 O(logn) 不会自动平衡
> 当插入节点为有序序列时，构建的树上的节点只有左孩子或右孩子，BST 将会退化为单向链表,最大复杂度O(N)。
#### AVL
> AVL (平衡二叉树) 是一 棵空树或它的左右两个子树的高度差的绝对值不超过1，并且左右两个子树都是一棵平衡二叉树。所有节点左右 -1 <= 平衡因子 <=1 平均复杂度O(logn) 旋转次数最多logn次

> 单旋转(zagzag全右/zigzig全左):从根节点开始到所要插入的结点的父节点,所经父节点都在同一条直线上.即所经父节点都在上一节点的左或右,则只需要进行一次旋转即可复平衡

> 双旋转:(zagzzig右左/zigzag左右):从根节点开始到所要插入的结点的父节点,所经父节点不在同一条直线上.此情况需要做两次旋转才可复平衡.

#### R-B tree
> (1) 根节点必须为黑色

> (2) 外部节点(新增为保证树平衡的节点/使之成为真二叉树)均为黑色

> (3) 其余节点: 若为红,则只能有黑孩子 //红之子、之父必黑 -- 控制红黑树深度

> (4) 任意外部节点到根: 经过的黑节点数目相等 //黑深度 -- 控制红黑树平衡

> 提升变换后(映射为4阶B-树/(2,4)树) 每颗红黑树都对应于一棵(2,4)树(B树)

> 旋转四种情况同AVL--不平衡才旋转:

> zagzag zigzig zagzig zig/zag

<table><thead><tr><th>插入方式</th><th>描述</th><th>旋转方式</th></tr></thead><tbody><tr><td>LL</td><td>在 a 的<strong>左子树</strong>根节点的<strong>左子树</strong>上插入节点而破坏平衡</td><td>右旋转</td></tr><tr><td>RR</td><td>在 a 的<strong>右子树</strong>根节点的<strong>右子树</strong>上插入节点而破坏平衡</td><td>左旋转</td></tr><tr><td>LR</td><td>在 a 的<strong>左子树</strong>根节点的<strong>右子树</strong>上插入节点而破坏平衡</td><td>先左旋后右旋</td></tr><tr><td>RL</td><td>在 a 的<strong>右子树</strong>根节点的<strong>左子树</strong>上插入节点而破坏平衡</td><td>先右旋后左旋</td></tr></tbody></table>
---

插入操作-双红缺陷 -- 违反//红之子、之父必为黑 规则.

情况1: 父、子双红

> 将该冲突部分子树中序遍历重新染色 使其在中序序列中恢复RBR这一模式.

情况2 : 叔、父双红

> 将叔、父节点均染成黑色

> 双红缺陷非法的原因: 提升变换后,在某个三叉节点中插入红关键码,使得原黑关键码不在居中 //RRB或BRR,出现相邻红色关键码.调整后的效果相当于提升变换后的B-树拓扑结构不变,但在新的四叉节点中,三个关键码的颜色改为RBR.
---

删除操作-双黑缺陷(提升转换后对应下溢缺陷)

情况1: 兄弟节点至少还有一个红孩子

> 删除该节点后通过一次zag/zig旋转即可修复.

情况2: 父节点为红色 兄弟节点均为黑色

> 删除该节点后,将父节点染为黑色,兄弟节点染为红色.

情况3: 父节点、兄弟、当前节点都是黑色

> 删除该节点后将兄弟节点染为红色.

情况4: 父节点、当前节点均为黑色,当前节点为红色

> 将父节点与当前节点颜色对换,父节点做一次旋转操作,在经过一轮情况1或2的重染色即可完成修复.

### B-Tree[B族搜索树]
#### B+[扩展]
#### B-[扩展]
#### B*[扩展]
#### 替罪羊树
#### 字典树
#### 树构建[扩展]
### 查找
#### 二分查找
```C++
int find_bin(int target,int arr[],int start,int end)
{
	int rankMid = (start+end)/2;
	if(target == arr[rankMid]) return rankMid;
	if(target < arr[rankMid]) find_bin(target,arr,start,rankMid);  
	if(target > arr[rankMid]) find_bin(target,arr,rankMid+1,end);
}
```

#### 线性查找-lineselectO(kn)[扩展]
### 索引
#### hashTable
散列冲突
> M = 90001 hash(key) = key % M

> 1%10 = 11%10 -> 5153.1876 %90001 = 6278.2001%90001

> 解决办法 将装填因子(装填元素个数/表总容量)降低 或者加长散列表.常规的操作是，当装填因此大于0.7时，就应该进行扩充了.

### B-Tree[B族搜索树]
#### B-tree
> 平衡的多路搜索树.

>在多级存储系统中使用B-树,可针对外部查找,大大减少I/O次数.批量访问,超级节点.

> m阶-m路 

> 上限:内部节点各有不超过m-1个结点的关键码 不超过m个分支.
>下限:树根分支树:节点数至少为2, 2<=n+1 其余节点分支数n+1 >= m/2上取整

> 插入会发生上溢[小概率]-分裂 删除会发生下溢[小概率]-借出关键码/合并

> B树长高:[再分裂] 发生上溢且上溢情况传播到根节点,这时可将第一次发生上溢的节点取其中位数作为新子树的根节点,连入原B树中.
#### B+tree
> B+相较于B树B+每个非叶子节点存储的关键字数更多，树的层级更少所以查询数据更快；树叶子节点的关键字从小到大有序排列，左边结尾数据都会保存右边节点开始数据的指针。B+树所有的叶子节点数据构成了一个有序链表，在查询大小区间的数据时候更方便，数据紧密性很高，缓存的命中率也会比B树高。

> B+树查询速度更稳定：B+所有关键字数据地址都存在叶子节点上.
### 八大排序[按考察重点排序]
#### Quick Sort

```C++
void QuickSort(int arr[],int L,int R)
{
  int i,j,key;
  i = L;
  j = R;
  key = arr[(L+R)>>1];
  while(i<=j)
  {
    while(arr[i] < key) i++;
    while(arr[j] > key) j--;
    if(i <= j)
    {
      std::swap(arr[i],arr[j]);
      i++;
      j--;
    }
  }
  // 左部分递归
  if(L < j) //防止越界判断
    QuickSort(arr,L,j);
  // 右部分递归
  if(i < R) //防止越界判断
    QuickSort(arr,i,R);
}
```

#### Shell Sort
> Tip:分割 嵌套调用其他算法.

```C++
void ShellSort(std::vector<int>& arr, int low, int high)
{
	int mid = (low + high) >> 1;

	if (low == high) return;

	ShellSort(arr, low, mid);
	ShellSort(arr, mid + 1, high);

	BubleSort(arr, low, high);
}
```

#### Merge Sort
```C++
void Merge(std::vector<int>& arr,int L,int mid, int R)
{
	//std::cout << "L<"<<L << "> m<"<<mid <<"> R<" << R << ">"<<std::endl;
	std::stack<int>Lstack, Rstack;

	int m = mid;
	int tl = L;
	int tr = R;

	// 左部分入栈 [L - mid] // [小-大]从右往左入栈
	while (L <= mid)
	{
		Lstack.push(arr[mid]);
		mid--;
	}

	// 右部分入栈 (mid - R] // [小-大]从右往左入栈
	m++;
	while (m <= R)
	{
		Rstack.push(arr[R]);
		R--;
	}

	// 左右比较 出栈 归并
	while (true)
	{
		// 左右比较 出栈
		if (!Lstack.empty())
		{
			if (!Rstack.empty())
			{
				if (Lstack.top() < Rstack.top())
				{
					arr[tl] = Lstack.top();
					Lstack.pop();
					tl++;
				}
				else
				{
					arr[tl] = Rstack.top();
					Rstack.pop();
					tl++;
				}
			}
			else
			{
				arr[tl] = Lstack.top();
				Lstack.pop();
				tl++;
			}
		}
		else
		{
			if (!Rstack.empty())
			{
				arr[tl] = Rstack.top();
				Rstack.pop();
				tl++;
			}
		}
		
		if (Lstack.empty()&&Rstack.empty())
			break;
	}
}

void MergeSort(std::vector<int>& arr, int L, int R)
{
	int mid = ((L + R) >> 1);
	if (L == R) return;

	MergeSort(arr, L, mid);
	MergeSort(arr, mid + 1, R);

	Merge(arr, L, mid, R);
}

```

#### Heap Sort
#### Insert Sort
```C++
void InsertSort_v2(std::vector<int>& arr, int low, int high)
{
	for (int i = low; i < high; i++)
	{
		for (int j = i+1;j<=high;j++)
		{
			// 和前面有序序列比较 插入
			int n = i;
			while (n>=low)
			{
				if(arr[n] > arr[j])
					std::swap(arr[n], arr[j]);
				n--;
			}
		}
	}
}

void InsertSort(std::vector<int>& arr, int low, int high)
{
	//6, 1, 3, 9, 2
	// 从第二开始左往右拿牌 并向左比较插入
	for (int i = low+1; i < high + 1; i++)
	{
		if (arr[i] < arr[i - 1])
		{
			int k = i;
			while (k>0)
			{
				if (arr[k] < arr[k-1])
				{
					std::swap(arr[k], arr[k - 1]);
				}
				k--;
			}
		}
	}
}
```
#### Select Sort
```C++
// 选择最值 往未维护序列的最左或最右末尾元素交换
void SelectSort(std::vector<int>& arr, int low, int high)
{
	for (int i = low; i < high + 1; i++)
	{
		int index = i;
		for (int j = i+1; j < high+1; j++)
		{
			if (arr[j] < arr[index])
			{
				index = j;
			}
		}
		std::swap(arr[i], arr[index]);
	}
}
```
#### Buble Sort
```C++
void BubleSort(std::vector<int>& arr, int low, int high)
{
	for (int i = low; i < high;i++)
		for (int j = low; j < high; j++)
			if (arr[j] > arr[j+1])
				std::swap(arr[j], arr[j+1]);
}
```

#### Bucket Sort
#### Bitmap Sort
!!!记住 一个字节 = 8 位!!!
#### Sort algorithem stablitiy
#### 时间复杂度
### 算法思想
#### Enum
#### Recursion
#### Divide and Conquer
#### Decrease and Conquer(pruning)
#### DP(0-1pakge 8-queue Fibonacci[斐波那契] step[台阶问题-爬楼梯] 图DP-走到某处花费最小代价 最短编辑距离 找零钱)
Fibonacci
```C++
// 输出 n 内的斐波那契数列
void Fibonacci_DP(int n)
{
	int res[2]{ 0,1 };
	int i = 2;
	while (res[(i % 2)] < n)
	{
		std::cout << res[(i % 2)] << " ";
		res[(i % 2)] = res[0] + res[1];
		i++;
	}
}
```
Upstairs

 有 1 或 2 两种步长 到第n级台阶有多少种走法

> Tip: 若只有 1 2 两种 步长 则为 经典斐波那契问题,即 第n级台阶 即为斐波那契数列的第n+4项 
```C++
// v1 source
void Upstair_DP_Fibonacci(int n)
{
	int res[2]{ 0,1 };
	int i = 2;
	while (i < (n+4))
	{
		std::cout << res[(i % 2)] << " ";
		res[(i % 2)] = res[0] + res[1];
		i++;
	}
}
// v2
void Upstair_DP(int n)
{
	int res[2]{ 1,2 };
	int i = 2;
	while (i < (n+2))
	{
		std::cout << res[(i % 2)] << " ";
		res[(i % 2)] = res[0] + res[1];
		i++;
	}
}

```
0-1 pakge

>Tip:DP 二维表
```C++
void Knapsack()
{
	std::vector<int> price{ 3,1,5,6,9 };
	std::vector<int> weight{ 1,4,3,2,2 }; // 1 + 2 -> 3 + 9 = 12
	const int _capacity = 3;
	int table[5][_capacity];
	
	// 初始化列
	for (int i = 0; i < _capacity; i++)
		if (i+1 >= weight[0]) table[0][i] = price[0];
		else table[0][i] = 0;
	// 初始化行
	for (int i = 1; i < weight.size(); i++)
		if (weight[i] > 1) table[i][0] = table[i - 1][0];
		else table[i][0] = std::max(table[i-1][0], table[i - 1][0]+price[i]);
	
	// 列
	for (int capacity = 1; capacity < _capacity; capacity++)
	{
		for (int row = 1; row < weight.size(); row++)
		{
			if (weight[row] > capacity) //不拿: 新增加的容量还是放不下这件物品继承上方的最优记录
			{
				table[row][capacity] = table[row - 1][capacity];
			}
			else //拿: 新增加的容量可以放下这件物品 最优解:max(上方的记录,当前容量 - 占用该物品容量 的最优记录 +当前物品)
			{
				table[row][capacity] = std::max(table[row - 1][capacity], table[row - 1][capacity - weight[row]] + price[row]);
			}
		}
	}
	std::cout << table[4][2] << std::endl;
}
```

完全背包(指定某件物品数量为无限)

> Tip:

> 不拿: 新增加的容量还是放不下这件物品继承上方的最优记录

> 拿: 新增加的容量可以放下这件物品 最优解:max(上方的记录,当前容量 - 占用该物品容量 的最优记录 +当前物品价值 + 剩余容量装下 指定物品个数*价值[此处需要回头查表计算剩余容量是否能装下 指定的物品,并计算能装几个,装下指定物品的总价])

混合背包
>Tip: 思路同上完全背包，最优解:max(上方的记录,当前容量 - 占用该物品容量 的最优记录 +当前物品价值 + 剩余容量装下 剩余容量的最优解 [此处需要回头查表 剩余容量能装下物品价值的最优解])


凑硬币硬币问题(用最少硬币凑出指定数额)
> Tip:打表 一维数组 前一个的最优解+1 即为 当前最优解
```C++
// Gather together a coin
// 举个例子:
// coins{1,2,3,5}
// 找币记录(所需硬币最少个数)res[]: 0 1 1 1 2 1 2 2 2 3 2
//                下标(待找面额):  0 1 2 3 4 5 6 7 8 9 10
// 前提:n>=coins[i]
// 转移公式 res[n] = min(res[n - res[n - 1]]+1/*待找数额的前一条记录*/,res[n - coins[i]] + 1/*枚举硬币面额小于等于待找数额的找币最优记录并+1: 当前面额 - 硬币面额coins(i) +1*/)
int Conis(std::vector<int>& coins, int amount)
{
	std::vector<int> res{0,1};
	res.resize(amount + 1);
	int n = 2;
	while (n <= amount)
	{
    // 默认取 前一记录+1 为当前最优解
		int min = res[n - res[n - 1]]+1;
		for (int i = 0;i<coins.size();i++)
		{
      // 状态转移 在小于等于待找面额的硬币中找面值最接近的硬币的找币记录的最优解
			if (n>=coins[i])
			{
				min > res[n - coins[i]] + 1 ? (min = res[n - coins[i]] + 1) : min;
			}
		}
    // 最优解 = min(前一记录,在小于等于待找面额的硬币中找面值最接近的硬币的找币记录的最优解)
		res[n] = min;
		n++;
	}
	return res[amount];
}

int main(int argc, char*args[])
{
	std::vector<int> coins{ 1,2,3,5 };
	std::cout << Conis(coins, 10)<<std::endl;
}

```

8-queue

>Tip : O(n^2) 堆栈法. 二维数组遍历 堆栈 棋盘染色 回溯
```C++
```

#### Traceback (DFS迷宫、DFS最短路、[DFS A-B 所有路径])
#### Branch and Bound
#### Greed(最小生成树[prime Kuskal]、Dijkstra最短路径)
#### 概率算法(求PI)
```C++
void getPi(int k)
{
  double sum = 1.0;
  int n = 1;
  while(n<=k)
  {
    sum+=pow(-1,k)*(1/((2*k)+1))
  }
  return sum*4.0;
}
```
---

## Cplusplus
### 关键字
#### namespace
> namespace通常用来给类或者函数做个区间定义，以使编译器能准确定位到适合的类或者函数.
---

#### auto
> auto可以在声明变量的时候根据变量初始值的类型自动为此变量选择匹配的类型.
---

#### const
> 用法1：const修饰函数传入参数 指针或是引用时便是不允许修改

> 用法2：修饰函数返回值 可以阻止用户修改返回值,返回值也要相应的付给一个常量或常指针。

> 用法3：const修饰成员函数(c++特性)

> const对象只能访问const成员函数，而非const对象可以访问任意的成员函数，包括const成员函数；

>const对象的成员是不能修改的，而通过指针维护的对象确实可以修改的；

> const成员函数不可以修改对象的数据，不管对象是否具有const性质。编译时以是否修改成员数据为依据进行检查。
---

#### virtual
> c++中的关键字“virtual”主要用在两个方面：虚函数与虚基类。

> 用于虚函数: 虚函数源于c++中的类继承，是多态的一种.且继承的子类必须实现父类中的虚函数.非虚函数是静态编译的时候就已经生成了,虚函数由运行时决定.

> 内联(inline)函数不能是虚函数，因为内联函数不能在运行中动态确定位置。

> C++中的虚函数的作用主要是实现了多态的机制。关于多态，简而言之就是用父类型的指针指向其子类的实例，然后通过父类的指针调用实际子类的成员函数

> 虚函数（Virtual Function）是通过一张虚函数表来实现的。每个父类都有自己的虚表.在表中，主是要一个类的虚函数的地址表，这张表解决了继承、覆盖的问题，保证其真实反应实际的函数。这样，在有虚函数的类的实例中这个表被分配在了这个实例的内存中.

虚函数其他

1.虚函数是可以递归调用的;

构造函数和析构函数中是可以调用析构函数的.但都不会触发多态.

> 构造函数中调用析构函数不会触发多态.此时子类还没有构造，所以此时的对象还是父类的，不会触发多态。

> 析构函数中调用虚函数不会触发多态.析构函数也是一样，子类先进行析构，这时，如果有virtual函数的话，子类的内容已经被析构了，C++会视其父类，执行父类的virtual函数。

---
#### inline
> 内联函数和普通函数的区别在于：当编译器处理调用内联函数的语句时，不会将该语句编译成函数调用的指令，而是直接将整个函数体的代码插人调用语句处.内联函数的调用不需要付出执行函数调用的额外开销.
---
#### explicit
> 默认类构造函数使隐式(默认有 implicit 关键字修饰)的即 Mystring str = "str" 编译器会自动转换为 Mystring str("str") explicit关键字的作用就是防止类构造函数的隐式自动转换. 被explicit修饰后的构造函数将不再允许隐式转换 只能显式调用Mystring str("str").

> [!注意:explicit 只在修饰单参数构造函数才有效果.]

返回对象的函数不调用拷贝构造函数?
> 拷贝构造函数前加 “explicit” 关键字；这样拷贝构造函数就不会进行自动类型转换，也就不会实现拷贝构造函数的调用了
---

#### export[扩展]
> 对模板类型，则必须在定义这些模板类对象和模板函数时，使用标准 C++ 新增加的关键字 export（导出）。
---
#### mutable[扩展]
### inline函数与有参宏
> inline C有参宏的替代
---
### 指针与引用
指针与引用区别
> 指针 :指针是一个变量，只不过这个变量存储的是一个地址，指向内存的一个存储单元；指针可以有二级指针引用没有,指针可以不赋初值;引用必须有明确引用对象.作为函数参数是传递进来的是实参的地址.

> 引用原变量的别名;作为函数参数时传递进来的是实参本身.

指针引用
> 

---

### NULL与nullptr 区别
NULL
> 在标准C库文件定义中 NULL 本质是一个宏 其定义的值为 0

nullprt C++11
> 指针字面量 nullptr C++11 中的关键词 C++11起 将NULL 宏定义为了 nullptr
### const sizeof const与引用
### this指针
> this 是一个 const 指针,是一个隐式形参,C++中的关键字,它指向当前对象，通过它可以访问当前对象的所有成员。函数中,成员变量和形参同名时(this->name = name),只能通过过指针区分.否则将会出现将成员变量值赋给形参这一情况.

> this 只能在成员函数内部使用，用在其他地方没有意义，也是非法的.只有当对象被创建后 this 才有意义，因此不能在 static 成员函数中使用.

### 什么是面向对象
> 面向对象是一种对现实世界理解和抽象的方法、是通过将需求要素转化为对象进行问题处理的一种思想。面向对象的三个基本特征是：封装、继承、多态。

封装
> (1)封装：封装是实现面向对象程序设计的第一步，封装就是将数据或函数等集合在一个个的单元中（我们称之为类）。封装的意义在于保护或者防止代码（数据）被我们无意中破坏。

继承
> (2)继承：继承主要实现重用代码，节省开发时间。子类可以继承父类的一些东西。


### 封装(pubilc protect private)
> 封装：!!!隐藏对象的属性和实现细节!!!，仅对外公开接口和对象进行交互，将数据和操作数据的方法进行有机结合.

> 注意：访问限定符本质上是给编译器使用的，数据放在内存中是没有任何限制的.
---

### 继承(多路径继承、虚继承[虚函数 纯虚函数 虚基类 虚析构的作用])
> 继承机制是面向对象程序设计使代码可以复用的最重要的手段，它允许程序员在保持原有的特性基础上进行扩展，增加功能，这样产生新的类，称作是派生类.继承是类设计层次的复用.

继承的三种方式

公有继承(public): 
> 父类公有仍为公有 - 父类保护仍是保护 - 父类私有仍是是私有,且基类不可访问.

保护继承(protected):
> 父类公有变保护 - 父类保护仍是保护 - 父类私有仍是私有,且基类不可访问.

私有继承(private):
> 父类公有变私有 - 父类保护变私有 - 父类私有仍是私有,且基类私有不可访问.

多继承
> 多继承注意二义性问题.存在父类也存在继承时,子类访问爷爷辈的基类成员要用域运算符指明访问的时父类的成员还是爷爷辈的成员 如
```C++
A(_a : int)->B(_a : int)->C; 
C(a : int){_a = a}; //这句换会报错, 产生歧义不知道访问的时 B 基类中的 属性_a 还是 A基类中的 属性_a 需要用域运算符指明.
C(a : int){A::_a = a};// 正确写法
```

虚继承
> 为了解决多继承时的命名冲突//二义性问题 和冗余数据问题，虚继承的最终派生类中只保留了一份虚基类的成员，所以该成员可以被直接访问，不会产生二义性.不论虚基类在继承体系中出现了多少次，在派生类中都只包含一份虚基类的成员.

虚函数作用
> 1.父类的情况:作为已定义的接口,强制子类必须实现.

> 2.作为虚析构函数,有父类指针持有在堆上的子类实例时,将父类析构函数设为虚析构函数能确保子类正确析构,防止内存泄漏.若父类虚构函数不是虚析构函数在子类析构时,只是虚构了父类,子类却不会正确虚构,这将导致内存泄漏.-- 解决办法,将父类析构函数改为虚析构函数.


### 虚基类中的虚函数表指针
> 若父类有虚函数,则在对象占用的内存块中的最前放还会有一个隐藏的虚基类表指针(虚函数表指针存储着虚函数表的地址),这是 多态(虚函数) 的实现关键.

> 多态正式由虚基类表指针指向的虚函数表所实现.

### 虚函数表
> 虚函数表是一块连续的内存空间,存储的是虚函数的函数入口地址.

虚基类的继承是多态的确切实施步骤,子类通过继承同样也会拥有了一个虚函数表指针,一个独立的虚函数表,在不重写的情况下,子类虚函数表所存储的函数入口地址与父类的表相同.若有重写,则会由重写的函数地址覆盖原父类函数入口的地址.

```C++
Class Base
{
pubilc:
int a = 1;

public:
virtual Func()
{
	// std::cout<<"Base Func. a = "<<a<<std::endl; // 通过函数指针直接持有表上函数地址是,是不带由实例属性的,因此不是实例调用函数.此句话 通过函数指针直接持有表上函数地址来直接调用词函数将会报错.
	std::cout<<"Base Func."<<std::endl;

}

Class InstanceA ：public Base
{
public:
InstanceA():a(2){}
virtual Func()
{
	// std::cout<<"InstanceA Func. a = "<<a<<std::endl;// 通过函数指针直接持有表上函数地址是,是不带由实例属性的,因此不是实例调用函数.此句话 通过函数指针直接持有表上函数地址来直接调用词函数将会报错.
	std::cout<<"InstanceA Func."<<std::endl;
	}
}

typedef void (*Func)() ;

Base base;
InstanceA instancea;

int* p = (int*)&base;
int* p1 = (int*)&instancea;

Func Funcptr_Base = (Func)*((int*)*p);
Func Funcptr_InstanceA = (Func)*((int*)*p1);

Funcptr_Base(); // call Base::Func();
Funcptr_InstanceA(); // call InstanceA::Func();
```



### 什么是多态
> 基类指针可以按照基类的方式来做事，也可以按照派生类的方式来做事，它有多种形态，或者说有多种表现方式，我们将这种现象称为多态.

#### 运行时多态

### 友元与运算符重载
友元
> 友元函数: 一个类的友元函数可以访问该类的私有成员.

> 友元类: 若A是B的友元类，则A的成员函数可以访问B的私有成员

运算符重载为友元函数
> !!![运算符为类的重载成员函数时不能满足需求，重载为普通函数又不能访问类的私有成员]!!!，此时需要将运算符重载为友元.

### 类拷贝(深拷贝、浅拷贝)
拷贝构造函数
> 第一个参数是自身类类型引用，其他参数都有默认值的构造函数就是拷贝构造函数.拷贝构造函数自己的参数必须是引用类型.
```C++
Sales_data::Sales_data(const Foo&){};
```

浅拷贝 (浅拷贝也叫位拷贝，拷贝的是地址)
> 浅拷贝在类成员中没有指针类型的成员时可以正常使用,但在有指针类型的成员时,浅拷贝中当前实例的指针类型成员若是直接由传入对象中的指针直接赋值,则会出现两个指针指向同一块内存的现象,通过其中一个指针去释放这块内存是另一指针将会变成野指针.

深拷贝 (深拷贝也叫值拷贝，拷贝的是内容)
> 深拷贝是为了避免在浅拷贝中两指针直接赋值使得两指针指向同一块地址这一问题(因为当通过其中一个指针释放指向的内存块时,另一指针将会成为野指针.),即新开辟一块内存将当前指针指向这块内存,并将传入对象中指针指向的内存中的内容也拷贝一份给当前指针指向的内存块.
```C++
// 深拷贝构造函数
Array::Array(const Array& rhs) {
		m_iCount = rhs.m_iCount;
		m_pArr = new int[m_iCount];
		for (int i = 0; i < m_iCount; i++)
		{
			m_pArr[i] = rhs.m_pArr[i];
		}
}
```
### C++智能指针
> 智能指针主要用于管理在堆上分配的内存，它将普通的指针封装为一个栈对象。当栈对象的生存周期结束后，会在析构函数中释放掉申请的内存，从而防止内存泄漏。

为什么要使用智能指针?
> 智能指针的作用是管理一个指针，因为存在以下这种情况：申请的空间在函数结束时忘记释放，造成内存泄漏。使用智能指针可以很大程度上的避免这个问题，因为智能指针是一个类，当超出了类的实例对象的作用域时，会自动调用对象的析构函数，析构函数会自动释放资源。所以智能指针的作用原理就是在函数结束时自动释放内存空间，不需要手动释放内存空间。

auto_ptr(C++11已弃用)
> C++98 中的解决方案,采用所有权模式.有内存泄露的潜在风险.
```C++
auto_ptr<string> p1 (new string ("I reigned lonely as a cloud.")); 
auto_ptr<string> p2; 
p2 = p1; //auto_ptr不会报错.
```
> 此时不会报错，p2 剥夺了 p1 的所有权，但是当程序运行时访问 p1 将会报错。所以 auto_ptr 的缺点是：存在潜在的内存崩溃问题！

share_ptr(共享指针)
> shared_ptr使用引用计数，每一个shared_ptr的拷贝都指向相同的内存。每使用他一次，内部的引用计数加1，每析构一次，内部的引用计数减1，减为0时，自动删除所指向的堆内存.

> 多个share_ptr可以指向同一个对象.循环引用会出现内存泄漏.即两个 shared_ptr 相互引用, 那么这两个指针的引用计数永远不可能下降为 0, 资源永远不会释放。

```C++ 
ptr_a-> m_bb_ptr = ptr_b;
ptr_b->m_aa_ptr = ptr_a;
```

unique_ptr(独占指针、同种有互斥属性)
> unique_ptr “唯一 ” 拥有其所指对象，同一时刻只能有一个unique_ptr实例指向给定对象（通过禁止拷贝、只有移动所有权move()函数来实现）。

weak_ptr
> weak_ptr 是一种不控制对象生命周期的智能指针, 它指向一个 shared_ptr 管理的对象.weak_ptr 是用来解决 shared_ptr 相互引用时的死锁问题.弱指针不会增加指向对象的引用计数,也不会对引用对象的内存进行管理,但弱引用指针会检测所管理的对象是否已经被正确释放.

```C++
class B;	//声明
class A
{
public:
	shared_ptr<B> pb_;
	~A()
	{
		cout << "A delete\n";
	}
};

class B
{
public:
	shared_ptr<A> pa_;
	~B()
	{
		cout << "B delete\n";
	}
};

void fun()
{
	shared_ptr<B> pb(new B());
	shared_ptr<A> pa(new A());
	cout << pb.use_count() << endl;	//1
	cout << pa.use_count() << endl;	//1
	pb->pa_ = pa;
	pa->pb_ = pb;
	cout << pb.use_count() << endl;	//2
	cout << pa.use_count() << endl;	//2
}

int main()
{
	fun();
	// fun 函数结束时意味着 类A B的实例生命周期已结束
	// 但由于 循环引用 使得二者的引用计数 仍不为0 所以 A B的实例并未正确析构.
	
	//解决办法:
	// 将类 A 或者B中的共享指针share_ptr 改为 弱引用指针 weak_ptr.
	return 0;
}
```

原理:

　　对于弱引用来说, 当引用的对象活着的时候弱引用不一定存在. 仅仅是当它存在的时候的一个引用, 弱引用并不修改该对象的引用计数, 这意味这弱引用它并不对对象的内存进行管理.
　　weak_ptr 在功能上类似于普通指针, 然而一个比较大的区别是, 弱引用能检测到所管理的对象是否已经被释放, 从而避免访问非法内存。

### C++11四种类型转换(static_cast dynamic_cast const_cast reinpreter_cast)
const_cast
> 去const 属性.解除const，volatile修饰符，只能转换指针或者引用.

static_cast
> 静态转换,对应于C的隐式转换,但转换双方必须在一个层级,比如 变量和指针间转换 (变量和指针不在同一层级).

dynamic_cast

有条件转换，动态类型转换，运行时检查类型安全(转换失败返回NULL).

> 1.用于基类和子类之间的安全转换.

> 2.必须有虚函数.

> 3.同基类的子类间的交叉转换,但结果返回空.

reinterpret_cast
> 将一种类型转化为另一种不相关的类型,对应C的强制转换.

> Tip:强制转换的代码是不可移植的，而且有时会产生不确定的结果.

语法格式
> TYPE B = x_cast(TYPE)(a);

### class与struct区别
C语言中struct
> struct没有继承. 不能有成员函数.不能有静态成员.struct 默认访问控制属性 public 且不能修改 而 class 默认访问控制属性时 private.不能在结构体中直接初始化数据成员.

### static与this指针
> 没有静态的this指针

### STL使用
#### STL主要有什么
> STL包括6部分内容:
> （1）容器（containers）：是一种数据结构容器，使用类模板的方式提供，我们可以方便的进行数据的存储操作。STL中，容器分为两类：顺序容器和关联式容器。 

>（2）适配器（adapters）：以序列式容器为基础，提供的栈，队列和优先级队列的这种容器。---也是一种容器

>（3）迭代器（iterators）：类似于指针，用来操作容器的对象。

>（4）算法（algorithm）：包含一系列的常见算法。

>（5）空间配置器（allocator）：其中主要工作包括两部分：1，对象的创建与销毁。2，内存的创建与释放。

>（6）仿函数（functor）：仿函数又称为函数对象，其实就是重载了()操作符的struct，没有什么特别的地方。---一大堆重载的操作符

set：其内部元素会根据元素的键值自动被排序。区别于map，它的键值就是实值，而map可以同时拥有不同的键值和实值。
#### Vector 扩容
vector
> 它是一个动态分配存储空间的容器。区别于c++中的array，array分配的空间是静态的，分配之后不能被改变，而vector会自动重分配（扩展）空间。

vector扩容 1.5或者2倍扩容(扩容因子：1.5或2)
> vector::resize(size_t n); 指定的vector中当前的可容纳元素数量小于原来的容量则删除末尾部分.

> vector::reserve(size_t n) reserve方法被用来重新分配vector的容量大小；

#### iterator erase(iterator) 后返回下一个
> 迭代器提供了一种方法,使它能够通过迭代器访问容器所含的各个元素,但无需暴露该容器的内部结构,它将容器和算法分开,好让而这独立设计.

#### map
> std::map 是有序键值对容器，它的元素的键是唯一的.map 通常实现为红黑树.

#### set
> std::set 是关联容器，含有 Key 类型对象的已排序集.set 通常以红黑树实现. !!![std::set是一颗封装好的封装好的红黑树]!!!.

#### map/set list/vector 使用场景
map/set
> 查找较多 其他操作较少时用 map(数据类型为key-value时)/set(只有values的场景)

list/vector

list
> list 随机访问性能较差 但随机删除插入操作较快. 适用于 随机访问较少但其他操作较多的情况

vector
> vector支持按矢访问 随机访问性能较高 但非向量头或尾部位置的插入删除操作较慢. 适合在随机访问频率较高但随机插入删除较少的情况下使用.

#### STL源码[扩展]
###  new malloc alloc
###  delete free
###  string类实现
> Tip 注意几个友元操作符的重载. 比较运算符 ==  != > < 加号运算符 + 流入流出运算发 << >>
```C++
friend bool operator==(const MyString &str1,const MyString &str2);
friend bool operator==(const char *str,const MyString &str2);
friend bool operator==(const MyString &str1,const MyString *str2);
friend bool operator>(const MyString &str1,const MyString &str2);
friend bool operator>(const char*str1,const MyString &str2);
friend bool operator>(const MyString &str1,const char*str2);

friend MyString operator+(const MyString &str1,const MyString &str2);
friend MyString operator+(const char*str1,const MyString &str2);      //两个字符串进行相加
friend MyString operator+(const MyString &str1,const char*str2);
 
friend ostream & operator<<(ostream &os,const MyString &str);
friend std::istream & operator>>(std::istream & is, String & s);
```

### C++ 特性 
> 构造闭包：能够捕获作用域中的变量的匿名函数对象。
```C++
[ /*捕获*/ value_name  = & this] ( 形参 ) -> ret { 函数体 }
```
### C++ 编码规范(Google编码规范)[了解]
### Boost库[扩展]
> Boost C++ 库 是一组基于C++标准的现代库。
## Linux
### Linux开发环境
#### 常见命令
#### gcc编译器、动态链接库、静态链接
> ```gcc test.c [gcc test.o 直接生成可执行文件]``` 将test.c预处理、汇编、编译并链接形成可执行文件。这里未指定输出文件，默认输出为a.out。

gcc 选项
> -E :输出源码.c/.cpp经过预处理后生成xx.i文件.
> 
> -S :输出汇编文件
> 
> -C 将 xx.s 汇编文件编译后输出目标代码文件 xx.o
> 
> -O[n:1-3]指定编译优化级别
>
> -static 强制使用静态链接库.
---
> GCC 在链接时优先使用动态链接库，只有当动态链接库不存在时才考虑使用静态链接库，如果需要的话可以在编译时加上-static 选项，强制使用静态链接库.

gcc 动态链接库 .so

生成动态链接库
> Tip: -fPIC -share -o xxx.so

```gcc test_a.c test_b.c test_c.c -fPIC -shared -o libtest.so```

使用动态链接库
>Tip: -L _ -l_ -o
>
> /home/xiaowp/lib/ 目录下有链接时所需要的库文件 libfoo.so ，为了让 GCC 能够顺利地找到它，可以使用下面的命令 [gcc xx.c -L 路径 -l库名(除去前缀lib后的库名) -o 可执行文件名]：
```
gcc foo.c -L /home/justin/lib -lfoo -o foo
```

gcc 静态链接库 .a
```ar rcs  libxxx.a xx1.o xx2.o```

生成静态链接库
> Tip:将多个/单个 xx.o 目标代码文件 用ar命令打包转换成 xx.a 静态库文件

指定使用静态链接库
> Tip: -L _ -static -l_ -o 

```gcc foo.c -L /home/justin/lib -static -lfoo -o foo```

---

#### gdb
> 使可执行文件支持gdb: ```gcc -g 源文件.c -o 输出的目标文件```

 
```shell
gdb filename 启动GDB 载入程序
- l 查看程序(带行号) 
- start -run 开始运行
- b n 在n行处下断点
- n 下一步
- set var i=n 设置变量i 值为 n
- print var 打印变量var 的值
```

#### makefile
#### shell编程
#### Valgrind[了解]
> Linux下C++程序中的内存泄露检查工具.原理仿真环境调试.

### Linux系统编程
#### 底层文件操作(不带缓冲的文件)、基本操作、printf、fprintf、sprintf
### 进程
#### 进程的基本概念、fork、exec、进程的五种状态切换、exit、shell的实现、守护进程
> PCB(进程控制块)，程序段，数据段三部分构成了进程实体（又叫进程映像）。
>
> 程序段：描述进程本身要完成的功能；
>
> 数据段：程序加工的对象和场所；
>
> 进程控制块：内存中存储，记录进程生存周期内状态变化的存储区域。不同操作系统有不同的进程控制块格式和信息，但基本包括进程标识符，当前状态，现场保护区，存储指针，占用资源表以及进程优先级等信息。它是进程存在的唯一标志。

进程
> 程序执行时的一个实例,是资源分配的最小单位.PCB是进程存在的唯一标志。

进程五种状态(按生命周期开始-结束)
>创建态：进程正在被创建，系统为其初始化PCB，分配资源。
> 
>就绪态:已经具备运行条件,但由于没有空闲CPU,而暂时不能运行.没有获得CPU
>
>运行态:占有CPU,并在CPU上执行中.
>
>阻塞态: 因等待某一事件而不能运行.
>
>终止态: 进程正在从系统中撤销,回收进程持有的资源,撤销其PCB.

进程间通信
> 进程通信主要有三种方式
>
> (1) 共享内存
> 
> (2) 消息传递
> 
> (3)管道通信:管道只能采用半双工通信.若要实现同时双向通信则需要设置两个管道.各进程要互斥地访问管道.如果没写满，就不会允许读.如果没读空，就不允许写.管道本质是一块在内存中开辟的固定大小的缓冲区.

线程
> 程序执行的最小单位

fork()
> int pid fork(); fork() 成功后会返回一个从系统获得的进程ID.一个进程子拥有独立的PCB,有和父进程一样的代码段、数据段.父、子进程靠进程ID(PID)区分.
> getpid() 返回当前进程PID getppid() 返回父进程ID
>
> 读时共享,写时复制-[父进程在操作这个物理内存块时（比如修改变量的值），再复制该部分的实际物理内存到子进程中.这就是写时复制。]

vfork()
创建一个与父进程[共享]数据段的子进程.

clone()

父子相同处: 全局变量、.数据段、.代码段、栈、堆、环境变量、用户ID、宿主目录、进程工作目录、信号处理方式...

父子不同处: 1.进程ID   2.fork返回值   3.父进程ID    4.进程运行时间    5.闹钟(定时器)   6.未决信号集

exec函数族
> 系统调用,exec函数族就提供了一个在进程中启动另一个程序执行的方法.
> 
> exec l le lp exec v ve vp
> 
> 这6个函数中真正的系统调用只有execve，其他5个都是库函数，它们最终都会调用execve这个系统调用

exec() 函数 [系统调用]
>exit()就是退出，传入的参数是程序退出时的状态码，0表示正常退出，其他表示非正常退出，一般都用-1或者1.

exit()在结束调用它的进程之前，要进行如下步骤：
>1.调用atexit()注册的函数（出口函数）；按ATEXIT注册时相反的顺序调用所有由它注册的函数,这使得我们可以指定在程序终止时执行自己的清理动作.例如,保存程序状态信息于某个文件,解开对共享数据库上的锁等.
>
> 2.cleanup()；关闭所有打开的流，这将导致写所有被缓冲的输出，删除用TMPFILE函数建立的所有临时文件.
>
> 3.最后调用_exit()函数终止进程。

shell实现
> 父进程负责读取标准输入流 main(args[] : char* ) 中的命令
> 
> fork() 出的子进程负责系统调用.

守护进程
> 守护进程一般在系统启动时开始运行，除非强行终止，否则直到系统关机都保持运行。守护进程经常以root权限运行，因为它们要使用特殊的端口或访问某些特殊的资源.如msqld进程 httpd进程
> 
> 一个守护进程的父进程是init进程.

编写守护进程的一般步骤步骤：

> (1) 在父进程中执行fork并exit推出；
>
> (2) 在子进程中调用setsid函数创建新的会话；
>
> (3) 在子进程中调用chdir函数，让根目录 ”/” 成为子进程的工作目录；
>
> (4) 在子进程中调用umask函数，设置进程的umask为0；
>
> (5) 在子进程中关闭任何不需要的文件描述符
>
> (6) 处理SIGCHLD信号

僵尸进程
> 父进先比子进程先挂了，子进程将成为僵尸进程从而占用系统资源
---

### IPC
#### IPC基本概念、管道、信号(进程间异步通信机制)、消息队列、内存共享、信号量(信号灯)

什么是IPC
> linux下的多个进程间的通信机制叫做IPC,它是多个进程之间相互沟通的一种方法.

linux下多种进程间通信的方法：
> 半双工管道、命名管道、消息队列、信号、信号量、共享内存、内存映射文件，套接字等等.

管道
> 半双工
> 
> 只能和具有亲缘关系的进程通信
> 
> 管道是由内核管理的一个缓冲区,只能在本地计算机使用.

命名管道
> 允许没有亲缘关系的进程间通信

管道与命名管道区别
> 管道只能由程序创建只能和有亲缘关系的进程通信,而命名管道可以用 ```mkfifo _fifoName_```命令提前创建好,进程只要调用文件操作函数即在命名管道中读写数据.

> 二者默认读写模式是阻塞的,若想设为为阻塞读写,则只需在调用```open()```函数时将参数设置为非阻塞```O_NONBLOCK``` .

信号
> 信号是进程间通信机制中唯一的异步通信机制；信号机制是进程间传递消息的一种机制，是异步进程中通信的一种方式.
> 处于执行状态的进程,信号会被优先处理.

进程间异步通信机制 
> 如果该进程当前并未处于执行态，则该信号就由内核保存起来，直到该进程恢复执行再传递个它；
>
> 如果一个信号被进程设置为阻塞，则该信号的传递被延迟，直到其阻塞取消时才被传递给进程。
> 
> 有两种信号不能被忽略，分别是SIGKILL和SIGSTOP。因为它们向内核和超级用户提供了进程终止和停止的可靠方法.

消息队列
> 消息的链表，存放在内核中，一个队列由一个队列 ID 标识.

> 消息队列中的消息有特定的格式和特定的优先级（有不同类型的消息）
> 
> 消息队列独立于发送和接收进程。进程终止，消息队列及内容并不会删除
> 
> 消息队列可实现消息的随机查询，消息不一定要以先进先出的次序读取，也可以按消息类型读取
  
msgget()
> 创建一个新队列或打开一个存在的队列；

msgsnd()
> 向队列末端添加一条新消息；

msgrcv()
> 从队列中取消息

共享内存
> 两个或多个进程共享一个给定的存储区

> 共享内存是最快的一种 IPC

> 信号量 + 共享内存通常结合在一起使用，信号量用来同步对共享内存的访问(无锁化编程)

信号量
> 信号量是一种计数器，用于控制对多个进程共享的资源进行的访问。它们常常被用作一个锁机制，在某个进程正在对特定的资源进行操作时，信号量可以防止另一个进程去访问它。
> 
> 信号量是特殊的变量，它只取正整数值并且只允许对这个值进行两种操作：等待(wait)和信号(signal)。(P、V操作，P用于等待，V用于信号) p(sv):如果sv的值大于0，就给它减1；如果它的值等于0，就挂起该进程的执行 V(sv):如果有其他进程因等待sv而被挂起，就让它恢复运行；如果没有其他进程因等待sv而挂起，则给它加1 

> 简单理解就是P相当于申请资源，V相当于释放资源 

#### 多线程同步四种方式
> 互斥锁（互斥量） 读写锁  条件变量 信号量

### 死锁
#### 进程死锁的原因
> 1.进程竞争.

> 2.进程推进顺序非法.

#### 形成死锁的四个必要条件
> 互斥、请求保持、不可剥夺、环路

#### 死锁的处理
> 鸵鸟策略、预防策略、避免策略、检测与解除死锁
---

### IO多路复用
#### IO多路复用基本概念
> 多路IO流监控.

> IO多路复用的作用就是感知IO（可读可写是否出错）是否就绪.这一过程是非阻塞的.

#### 为什么使用IO多路复用?解决了什么问题?
> 多路IO复用是为了解决通过单个线程去记录追踪每一个文件描述符(IO流)的状态并同时管理多个IO流.

> IO多路服用模型只是做文件见描述符状态的确认,并不关系描述符数据是否否正在读取,通过这一机制解决了如果使用多线程和多进程监控多个文件描述符未就绪是造成的堵塞的情况.

能用多进程代替吗?
> 不能.因为开销大(撤销,上下文切换)且进程数量有限(系统可分配资源有限).与多进程和多线程技术相比，I/O 多路复用技术的最大优势是系统开销小，系统不必创建进程 / 线程，也不必维护这些进程 / 线程，从而大大减小了系统的开销。

能用多线程代替吗?
> 不能.IO操作可能会造成堵塞.若改为循环非阻塞状态下的操作,则会无法感知IO(描述符)状态.需要花费更多的CPU时间,效率不高.

### Linux socket编程
#### socket基本操作
#### select
select 1024限制

Linux:
```C
  #define __FD_SETSIZE    1024
```
> linux 内核限定了FD_SET 这一用于存储文件描述符的位图的大小就是1024.
>
> 1024是linux 约定的限制大小,对于大于等于1024的socket select 仍然支持注册进位图,但会出现不可预知的错误比如越界、数据覆盖等.

Linux下的解决办法
> 1.编译内核
> 2.自定义FD_SET 不适用系统内核提供的位图.

Windows:
> 直接在自己引入并修改Windows下的FD_SIZE宏定义即可
>
> Windows下的FD_SET是由数组实现的.

unix(macos)
> 在文件中引入 系统指定的两个宏中的其中一个即可突破1024限制
```c 
// 在select 实现文件中可以找到.
#define _USE_C_SOURCE_UMLIMIT
//或
#define _USE_......_UMLIMIT //记不清了
```
select 性能热点
```C
core_sys_select ()
```
这个函数主要功能是在实现真正的select功能前，准备好 fd_set ，即从用户空间将所需的三类 fd_set 复制到内核空间。从下面的代码中你会看到对于每次的 select系统调用，都需要从用户空间将所需的三类 fd_set 复制到内核空间，这里存在性能上的损耗。
> 1.轮询
> > 拷贝到内空间需要遍历一次(监控描述符状态,修改三大集合),拷到用户空间(遍历集合,取出)
>
> 2.每次调用select都做三大集合的拷贝 用户空间->内核空间
> 
> 3.每次select 返回后都会将以前加入但无事件发生的文件描述符清空.所以在下一次select开始前还需要将已接入的socket重新加入到集合中.

（2）将fd加入select监控集的同时，还要再使用一个数据结构array保存放到select监控集中的fd，一是用于再select 返回后，array作为源数据和fd_set进行FD_ISSET判断。二是select返回后会把以前加入的但并无事件发生的fd清空，则每次开始 select前都要重新从array取得fd逐一加入（FD_ZERO最先），扫描array的同时取得fd最大值maxfd，用于select的第一个 参数。

（3）可见select模型必须在select前循环array（加fd，取maxfd），select返回后循环array（FD_ISSET判断是否有事件发生）

解决办法

> 对于第3.
> 
> 可以做一个三大集合的备份,让select在副本中操作即可.下次直接恢复备份即可.位图置位操作性能消耗高于按矢访问操作.


#### epoll
> Epoll 的连接上线取决于 file-max.conf 配置文件中的软限制值、硬限制值和物理内存的大小.
> 
> 每个epoll对象都有一个独立的eventpoll结构体，用于存放通过epoll_ctl方法向epoll对象中注册进来的事件.这些事件都会挂载在红黑树中.添加到epoll中的事件都会与设备(网卡)驱动程序建立回调关系，也就是说，当相应的事件发生时会调用这个回调方法。这个回调方法在内核中叫ep_poll_callback,它会将发生的事件添加到rdlist双链表中。

epoll高效的原因
> 不重复传递socket句柄给内核，通过```epoll_ctl()```内核中红黑树存储要监控的句柄，当有事件发生时,epoll 不会遍历所有已注册的事件集合,而是从红黑树中找到该事件句柄,并通过双链表存储准备就绪的事件,epoll只将绪事件列表中的事件逐一处理即可.

水平触发[LT](epoll默认模式)
> 有事件发生,只要该事件未处理或未处理完(如数据未读完)就会再次通知(再次加入到就绪事件链表中)下次epoll_wait()时将会再次返回.优点:不会丢数据.缺点:只要未处理完就绪链表不为空就会一直通知.占用资源.

LT模式下，只要一个句柄上的事件一次没有处理完，会在以后调用epoll_wait时次次返回这个句柄，而ET模式仅在第一次返回。

边缘触发[ET]
> 事件发生就通知,只通知一次,未处理完不在通知.只有事件发生变化后才会再次发生通知(关注边际变化),比如一个socket由读状态转为写状态,此时才会将该事件再次加入到就绪链表中.优点:只通知一次,不会频繁唤醒进程,资源占用少.缺点:未处理时间若不及时处理会出现数据丢失.

#### 线程池
## Windows 
### Windows socket编程
#### IOCP
> Windows下的异步IO模型 是通过 主线程投递任务 ```PostQueuedCompletionStatus()```  -> 工作线程获取```GetQueuedCompletionStatus()```并处理任务并反馈作业消息 ->主线程接收通知并在此投递.异步地处理网络事件.

> 在调用 AcceptEx 接受连接后,每个连进来的socket都会绑定有一个重叠结构体.向系统投递任务这一结构体用来标识该任务时使用了异步机制,即表明该事件是IOCP事件.

重叠体(重叠结构体)
> 包含用于异步（或重叠）输入和输出 (I/O) 的信息.

AcceptEx 比 Accept 强三点：

>（1）最关键的是 AcceptEx 在客户端连入之前, 就把客户端的 Socket 建立好了, 也就是说, AcceptEx 是先建立Socket, 然后发出的 AcceptEx 调用, 也就是说, 在进行客户端的通信之前, 无论是否有客户端连入,Socket 都是提前建立好的, 而不需要像 accept 是在客户端连入之后, 在现场花费时间建立 Socket.


>（2）相比 Accept 只能阻塞方式建立一个连入的入口, 对于大量的并发客户端来讲, 会出先连入因为链接连接过度处理不过来时发生堵塞等待这一现象，而 AcceptEx 可以在完成端口上投递多个请求, 还有客户端连入的时候, 就非常从容地去接受连接.

>（3）AcceptEx 还有一个优点, 就是投递 AccepEx 的时候, 收取客户端发来的第一组数据, 这是同时进行的, 也就意味着, 如果客户端只是连入但不发送数据的话, 我们就不会收到这个 AccepeEx 完成的通知,异步的 AcceptEx 使用起来比 accept 要麻烦。

AcceptEx() 接受连接优化

> 不使用```WSAloctl()```函数将AcceptEx()加载到内存中的情况下,每次由连接连入系统都会从Mswsocket.lib中重新载入AcceptEx()函数处理连接.在由多个客户端频繁断开连入时,这样是十分低效率的.--来自MSDN.

解决办法
> 调用```WSAloctl()```函数预先将```AcceptEx()```一次性载入到内存当中,在再次发生调用时通过```lpfnAcceptEx``` 指针调用已加载到内存中的```AcceptEx()``` 来处理连接任务. --MSDN优化建议.

#### select
### select与Epoll区别
> （1）select，poll 只要读写事件发生就会不断轮询所有 fd 集合.而 epoll 其实也需要调用 epoll_wait 不断轮询的是就绪链表，是它是设备就绪时，调用回调函数，把就绪 fd 放入就绪链表中，并唤醒在 epoll_wait 中进入睡眠的进程。

> （2）select，poll 每次调用都要把 fd 集合从用户态往内核态拷贝一次，并对该集合进行遍历找出有读写事件的socket，而 epoll 在接受连接后只进行一次拷贝,即将新来连接注册进内核中用红黑树索引的集合中.
---

## 数据库
### 基本知识[待补充]
#### 三大范式
1NF(列不可再分)
> 表中所有字段都是不可再分割的原子项.(字段原子性)

2NF(属性完全依赖于主键)
> 在第一范式满足的条件下成立.每一列都必须完全依赖主键.只有在联合主键的情况下才会有不完全依赖.

3NF(属性不依赖于其它非主属性    属性直接依赖于主键)
> 在第二范式满足的条件下成立.除了主键列的其他类不能由传递依赖的关系.(数据不能存在传递关系，即每个属性都跟主键有直接关系而不是间接关系.)

例子

表:STU（学号，姓名，年龄，性别，所在院校，院校地址，院校电话）

> 存在传递依赖 学号--> 所在院校 --> (院校地址，院校电话) 这里的(院校地址并不直接能通过学号直接查询到,或者说(院校地址,院校电话)并不直接依赖于学号而是直接依赖于院校地址)

> 应修改为 （学号，姓名，年龄，性别，所在院校）--（所在院校，院校地址，院校电话）
#### SQL语句
#### MySQL基本用法
#### 索引机制-索引引擎[扩展]
常见存储引擎

InnoDB(MySQL默认)、MyISAM、Memory、NDB.

InnoDB
> MySQL默认存储引擎 支持事务、行级锁定、外键.采用聚簇索引.InnoDB默认使用B+树作为存储索引引擎.

InnoDB文件结构
> .frm 表信息包括表结构定义信息,创建表后产生此文件
> 
> .ibd/ibdata 数据文件

MyISAM
> 不支持事务.不支持外键.带有外键的InnoDB表转为MyISAM会失败.采用非聚簇索引.表级锁定.

MyISAM文件结构
> .frm 表信息包括表结构定义信息,创建表后产生此文件
> .MYD(MYDATA) MyISAM特有 存储表数据
> .MYI(MYINDEX) 存储索引信息.

执行 ```select count(*) from tablename;```那个引擎最快?
> MyISAM. MyISAM有一个变量专门保存数据行数.而 InnoDB 需要扫面全表后才能返回统计数.

char varchar 区别?

相同点
>char varchar 都会截断超过长度设定之后的字符.

不同点
> char, varchar 长度可变.
> 
> char 存储时会截断尾部空格.
> 
> char 存储上限255.

BLOB 和 TEXT 有什么区别？
> BLOB 保存二进制数据，TEXT 保存字符数据。

数据库索引的原理，为什么要用 B + 树，为什么不用二叉树？
> 等量数据情况下B-树的树高一定比二叉树更矮,所以IO磁盘I/O次数会更少.利用B-树超级节点批量加载的特性,减少I/O次数.

聚集索引与非聚集索引的区别？
> 1.聚集索引存储记录是物理上连续存在，而非聚集索引是逻辑上的连续，物理存储并不连续
> 
> 2.叶子节点存储内容不同.聚簇索引叶子节点就是数据节点(叶子节点存储的是完整的数据记录),而非聚簇索引叶子节点存储的是索引(主键值或时地址),所以非聚簇索引也叫二级索引, MyISAM 用的就是 非聚簇索引.

MySQL 索引
> B+树索引
> 
> hash索引
> 
> Full-Text 全文本索引
> 
> R-Tree 索引 (空间索引-MyISAM)

B+Tree 相对于 B-Tree 有几点不同：

>1.非叶子节点只存储键值信息；
> 
>2.所有叶子节点之间都有一个链指针；
>
>3.数据记录都存放在叶子节点中

为什么 Mysql 索引要用 B + 树不是 B 树？
> B + 树不用 B 树考虑的是 IO 对性能的影响，B 树的每个节点都存储数据，而 B + 树只有叶子节点才存储数据，所以查找相同数据量的情况下，B 树的高度更高，IO 更频繁。数据库索引是存储在磁盘上的，当数据量大时，就不能把整个索引全部加载到内存了，只能逐一加载每一个磁盘页（对应索引树的节点）。其中在 MySQL 底层对 B + 树进行进一步优化：在叶子节点中是双向链表，且在链表的头结点和尾节点也是循环指向的。
> 
为何不采用 Hash 方式?
> Hash 索引底层是哈希表，哈希表是一种以 key-value 存储数据的结构，所以多个数据在存储关系上是完全没有任何顺序关系的，所以，对于区间查询是无法直接通过索引查询的，就需要全表扫描。所以，哈希索引只适用于等值查询的场景。

哪些情况需要创建索引
> 1.主键自动建立唯一索引
> 
> 2.频繁作为查询条件的字段
> 
> 3.查询中与其他表关联的字段，外键关系建立索引

哪些情况不要创建索引
> 1.表记录太少
> 
> 2.经常增删改的表
> 
> 3.频繁更新的字段不适合创建索引（会加重 IO 负担）

#### 事务[扩展]
什么是事务?
> !!![事务就是为了保证一组数据库操作]!!!，要么全部成功，要么全部失败.

MySQL 三大问题 脏读 幻读 不可重复读

脏读
> 并发执行事务时: 读到未提交的的数据.

幻读
> 同样的操作,读到的记录数不同.


不可重复读
> 同一条语句查询到的结果不同.

---

## Redis
### Redis 基本知识

keys

keys 指令会导致线程阻塞一段时间，线上服务会停顿，直到指令执行完毕，服务才能恢复

scan

scan 指令可以无阻塞的提取出指定模式的 key 列表，但是会有一定的重复概率，在客户端做一次去重就可以了，但是整体所花费的时间会比直接用 keys 指令长.

set get

为什么要用Redis?
> 访问流量高峰等等，都很容易把数据库打崩，所以引入了缓存中间件，目前市面上比较常用的缓存中间件有 Redis 和 Memcached 不过中和考虑了他们的优缺点，最后选择了 Redis(其实就是因为Redis支持分布式<-_<-)。

redis 支持哪些数据结构?
> String(默认使用) Hash List Set SortedSet(还用过Redis Module - BloomFilter)

#### redis和memcached有什么区别?
> 1.redis 支持分布式.
> 
> 2.redis 支持更多的数据结构.和更丰富的操作.
> 
> 3.redis 支持直接在服务端操作数据,memcached不支持(需要拿到客户端来操作).

#### redis支持哪些数据结构
> String(默认使用) Hash List Set SortedSet(还用过Redis Module - BloomFilter)

#### redis有几种持久化机制?
持久化原理
> 数据快照.命令日志.

支持的持久化机制
> RDB(数据快照) AOP(命令日志).

RDB
> 恢复速度快, 但不支持实时特性,版本间不兼容.(默认开启) bgsave / save m n

AOF
> 支持实时特性,但恢复速度慢.

#### redis同步机制?[扩展]
#### 服务主从数据怎么交互的?[扩展]
#### BloomFilter
[只需确定确定误判率p  插入个数n] 哈希函数个数k 布隆数组长度m 通过公式代入p,n获得.M(n,p) = m, K(m,n) = k;
#### 对方追问那如果突然机器掉电会怎样？[扩展]
#### 大量key同时过期要注意什么?
> 大量key同时过期,造成redis暂时卡顿.在某些情况下还会造成缓存雪崩.
>
> 解决办法:为了不让大量key处于同一时间过期,造成redis卡顿,可以为每个key的过期时间加上随机值,使得过期时间分散些,降低redis服务器压力.

#### redis缓存雪崩
> Tip:大量合法数据由于缓存失效(缓存雪崩了)打到数据库.
>
> redis服务器中有一批key要在某一时刻过期,这是突然后大量请求突然涌入redis,涌入的请求本来应有redis响应的,但是由于这批key的过期,导致请求直接打到数据服务器上,导致数据服务器卡顿,或者崩溃.

#### 如何解决redis缓存雪崩?
> 为了不让大量key处于同一时间过期,可以为每个key在原有过期时间上加上一个随机值,使过期时间分散,降低redis服务器压力和后台数据服务器的压力./或者不设置过期时间.

#### 那你了解缓存穿透和击穿么，可以说说他们跟雪崩的区别么？
缓存穿透(直接穿透了缓存和数据服务器[<-数据库也没有]--非法数据打数据库)
> 缓存穿透是指缓存和数据库都没有的的数据,用户构造出这样的非法数据直接打到数据库上,以此造成服务器压力.严重的情况下会击垮数据库.

缓存击穿(一点破面,穿透了缓存--一条合法数据打数据库)
> 缓存击穿是指缓存中没有但数据库中存在的情况,由于这个key的实现导致带着这个key的请求直接打在了数据库上,攻击者用这个失效的key构造大量的请求包且同时地发送给服务器就会造成缓存击穿,就相当于在桶上造了个洞一样.

#### 如何解决缓存穿透[业务逻辑上拦截、高级点:bloom filter]
> 1.在业务逻辑上做校验拦截.比如写函数时不信任任何外部输入.
> 
> 2.使用bloom filter,把没有的统统挡回去.

#### 如何解决缓存击穿
> 1.设置热点数据永不过期.
>
> 2.及时亡羊补牢,一旦有请求直接落到数据库上,在返回响应数据的同时也将该返回数据及时加入到缓存中.

## QT
### QT基本知识
#### QT元对象系统
> Qt中的元对象系统是一个基于标准C的扩展，为Qt提供了信号与槽机制、实时类型信息、动态属性系统。元对象系统基于QObject类、Q_OBJECT宏、元对象编译器MOC实现。

QObject类
> 作为每一个需要利用元对象系统的类的基类.只有继承了QObject类才能使用元对象系统.

Q_OBJECT宏
> 定义在每个类的私有数据段,用来启用元对象功能,比喻动态属性,信号和槽.

元对象编译器(moc)
> 如果一个头文件包含Q_OBJECT宏定义,元对象编译器就会将该文件编译成C++源文件.该文件包括了Q_OBJECT的实现代码.新生成的文件名都会带有moc_前缀,表示是带有Q_OBJECT实现的源代码.

除了提供在对象间通讯的机制外，元对象系统还包含以下几种功能：

> QObject::metaObject()方法，获得与一个类相关联的meta-object。

> QMetaObject::className()方法，在运行期间返回一个对象的类名，不需要本地C++编译器的RTTI（run time type information）支持。

> QObject::inherits()方法，用来判断一个对象的类是不是从一个特定的类继承而来。

> QObject::tr()、QObject::trUtf8()，!!![为软件的国际化翻译字符串]!!!。

> QObject::setProperty()、QObject::property()，根据属性名动态的设置和获取属性值。

#### QT内存管理
Qt内存管理机制：

> Qt 在内部能够维护对象的层次结构。对于可视元素，这种层次结构就是子组件与父组件的关系；对于非可视元素，则是一个对象与另一个对象的从属关系。在 Qt 中，在 Qt 中，删除父对象会将其子对象一起删除.

QObject&parent 机制
> 使用元对象的类都是QObject的基类,QObject内部有一个表,会保存实际派生出的子类,还有一个指针保存parent,当(QObject类)自己析构时,会自己从parent列表中删除并析构所有的子类.

自动垃圾回收机制

Qt对象清理器是实现自动垃圾回收的很重要一部分. 

(1)QObjectCleanupHandler.

> QObjectCleanupHandler可以注册很多子对象，并在自己删除的时候自动删除所有子对象。同时，它也可以在程序运行时识别出是否有子对象被删除，从而将其从它的子对象列表中删除。这个类可以用于不在同一层次中的类的清理操作，例如，当触发关闭槽函数时关闭某窗口,某对象的析构.

(2) 计数器

(3) 记录所有者

#### QT信号与槽
信号与槽观察者模式的一种实现特性如下:
> a.信号就是能被具体观察到的事件,或者说是事件发生后的通知信息.

> b.槽函数是观察者

> c.信号与槽的连接形成了一种 被观察者-观察者 的关系.

> d.当事件发生或者状态改变,信号就会被发出;同时信号有义务去调用对该信号感兴趣的槽.

信号与槽是多对多的关系.信号是可以接力传递的.

####　连接函数第五个参数
```connect(const QObject *sender, const char *signal, const QObject *receiver, const char *method, Qt::ConnectionType type = Qt::AutoConnection)```

> Qt::ConnectionType type 枚举类型,默认是自动连接,用来确定连接类型.有唯一链接,堵塞连接,直接连接...

#### QT消息机制
> 最开始的Qt消息循环开始```QCoreApplication::exec()```。用户创建出一个QApplication，执行QCoreApplication::exec()，一个应用程序便开始了。QCoreApplication会不断从操作系统获取消息，并且分发给QObject。

如果没有消息循环，那么Qt的信号和槽无法完全使用，有些函数也无法正确执行。举个例子，通过```connect```连接的信号，当有信号发出时,其实是将一个事件压入了消息循环，如果没有QCoreApplication::exec()，那么这个消息循环将永远无法派发到指定的对象.

#### QT事件处理机制
> Qt事件是一个QEvent对象，用于描述程序内部(如定时器超时)和外部发生的动作，任何QObject对象都具备事件处理能力。

事件处理流程:
> 用户操作 --> 系统内核感知 -(os消息/信号)-> Qt 应用程序 -(Qt 预定义的信号)-> 对应对象(事件发生在Qweiget/QMainWindow/...那对应的对象就是Qweiget/QMainWindow/...)的Event函数对该事件处理.

#### QT多线程
>  QT通过三种形式提供了对线程的支持，分别是平台无关的线程类、线程安全的事件投递、跨线程的信号-槽连接

QThread

QThread是Qt线程中有一个公共的抽象类，所有的线程类都是从QThread抽象类中派生的，需要实现QThread中的虚函数run(),通过start()函数来调用run函数。

> ```void run()```线程体函数,用于定义函数功能.

> ```void start()```线程体函数的启动函数.用于将线程入口地址指向为```void run()```函数.

> ```void terminate()```函数用于强制结束线程,不保证数据完整性和资源释放.

当线程启动和结束时，QThread会发送信号started()和finished()，可以使用isFinished()和isRunning()来查询线程的状态。

QThread实现多线程两种方式:
> 1 继承QThread类重写run().

> 2 创建一个QThread对象 用_thread->moveToThread(QObject obj); 将作业实例依附到线程中, 并启动线程 _thread->start();

Qtconcurrent::run([](){}); 实现多线程

Qtconcurrent::run([](){}); //C++11匿名函数、多线程. 配合QThreadpool 可做作业线程池.

#### QT网络编程
> Qt网络模块为我们提供了编写TCP / IP客户端和服务器的类。 它提供了较低级别的类，例如代表低级网络概念的QTcpSocket，QTcpServer和QUdpSocket.
#### 软件发布
> Tip: windeployqt 虚拟盒子.
#### VS下的Qt
> Tip: Qt for vs qmake .
---

## 设计模式
### 设计模式基本知识
> 设计模式，指的是软件工程领域，人们为了解决某类软件设计开发的重复问题而总结出来的代码设计经验。

为什么要使用设计模式?
> 1.避免重复劳动,提高设计和开发效率.
>
> 2.设计模式提供了一套通用的设计语言,方便开发人员沟通交流.

设计原则七大原则
>1.单一职责原则: 一个类只负责一项职责.
>
>2.开放-关闭原则: 软件实体可以被扩展但不可以被修改.
>
>3.里氏替换原则: 派生类要遵守父类设计约束,不可对非抽象方法随意修改.
>
>4.依赖倒转原则: 抽象不应依赖细节,细节依赖于抽象.
>
>5.接口隔离原则: 类的依赖应尽可能简单.
>
>6.迪米特法则: 尽量少地暴露类的设计细节.
>
>7.组合/聚合复用原则: 尽量使用组合/聚合.继承会破坏封装性.

#### 单例模式(懒汉模式、饿汉模式)
> 目的保证该类的实例唯一性.--保证该类实例只有一个.

##### 懒汉模式
> 单例实例在使用时才创建.

> 饿汉模式是线程不安全的,如果两线程同一时刻调用接口获得实例就有可能会创建两个实例.

> 解决办法1.在创建实例时加锁.使创建实例的过程带有互斥特性.

> 解决办法2.C++11内部静态变量的懒汉单例.

##### 饿汉模式
> 饿汉模式,指系统一运行，就初始化创建实例，当需要时，直接调用即可。缺点，正是由于把实例对象放到堆内存中，这样应用一加载就会看到对应实例，极大浪费内存。

##### 单例模式线程安全问题

#### 工厂模式
> 定一个创建对象的接口,让子类自己决定实例化哪一个类.

#### 观察者模式
> 多个对象间存在一对多的依赖关系，当一个对象的状态发生改变时，所有依赖于它的对象都得到通知并被自动更新。这种模式有时又称作发布-订阅模式、模型-视图模式，它是对象行为型模式。

## git的使用
## UML
## 软件开发
### 软件开发基本知识
#### 软件开发流程
需求分析-->概要设计-->详细设计(coder 会拿到详细设计书)-->编码-->测试-->交付-->验收-->维护
#### 需求分析
#### 概要设计
#### 详细设计 coder拿到的
#### 编码 coder
#### 测试
## 计算机网络
### OSI七层模型与TCP/IP五层模型
OSI七层模型(自下而上):
> 物理层 -> 数据链路层 -> 网络层 -> 运输层 -> 会话层 -> 表示层 -> 应用层

TCP/IP五层模型
> 物理层 -> 链路数据层 -> 网络层(IP) -> 运输层(TCP/UDP) -> 应用层

### 三次握手

seq:包序列号

ack:包序列号确认号 (对端该发seq+1个数据包了-问对端要seq+1个数据包)

ACK:0[请求数据包] 1[确认数据包]

SYN: 只有在TCP 建立连接的前两次有意义 [即SYN=1]

TCP 连接请求 SYN=1 ACK=0[客户端第一请求]
TCP 连接确认 SYN=1 ACK=0[服务器返回第一次确认]
确认的确认、传输数据的TCP数据包 SYNC=0

>①[c -(SYN ACK seq我要链接咯)-> s] ②[s -(SYN ACK seq ack 你确定要链接吗?)-> c] ③[c -(ACK seq ack [确认]是的,我要链接.)->s ]
#### 为什么是三次握手而不是两次?
> “三次握手” 的目的是 “为了防止已失效的连接请求报文段突然又传送到了服务端，因而产生错误”。 -- 《计算机网络》 谢希仁著.

> TCP是全双工协议,任何信道的传输本身来说都不是绝对可靠的,为确保建立的信道可靠至少需要三次的确认性的通讯.第一次是发起者向接收者询问状态,第二次是接收者确认发起者状态,第三次则是双方达成协议.即发起者确认与接收者建立通讯.而在这三次确认性的通讯期间传输 SYN ACK seq ack 状态校验码值得变动便是双建立同时所做的数学上的协商校验.因为如果中间得校验码值在任何一方校验失败,此次通讯都不会被建立.

### 四次挥手
#### 为什么是四次挥手
> TCP连接是全双工的,因此每个方向都需要进行独立关闭.客户端从开始关闭到完全关闭中间会经历四次状态变动,分别是 ①[established->fin-wait-1] ②[fin-wait-1->fin-wait-2] ③[fin-wait-2->time-wait] ④[time-wait-closed]
服务端从开始关闭到完全关闭中间会经历三次状态变动: ①[established-close-wait] ②[close-wait-last-ack] ③[last-ack-closed]
四次挥手是双方状态相互确认的一个过程中间缺一不可.

> C: established -> fin-wait-1 -> fin-wait-2 -> time-wait -> closed.

> S: established -> close-wait -> last-ack -> closed.
### TCP
#### TCP和UDP区别
①TCP是面向连接的通讯的,TCP是长连接,UDP是短连接

②TCP是1对1连接,UDP可以是多对多交互通讯

③TCP是可靠传输因为建立连接和关闭连接前会双方都会做对自身和端状态确认.UDP则没有这一过程,所以UDP是不可靠传输.

④TCP是面向字节流传输,UDP是面向报文传输.

⑤TCP首部开销大于UDP首部开销.

#### TCP滑动窗口协议
> 滑动窗口解决的是流量控制的的问题，就是如果接收端和发送端对数据包的处理速度不同，如何让双方达成一致。窗口大小代表了设备一次能从对端处理多少数据，之后再传给应用层。缓存传给应用层的数据不能是乱序的，窗口机制保证了这一点。

#### TCP握手以及每一次握手客户端和服务器端处于哪个状态（11种状态）
#### TCP怎么保证可靠性（面向字节流，超时重传，应答机制，滑动窗口，拥塞控制，校验等）？
> 1.TCP是面向字节流的通讯.

> 2.TCP通讯时设立的多种校验机制和拥塞控制、超时重传等机制保证.

#### TCP/IP的分片粘包过程
> TCP对于发送缓冲区数据发送并不是即时发送的,而是定时定量发送的,即数据在一定时间内发送缓冲区内的数据如果大到发送大小就会立即发送并不会关进数据包是否完整.在这样的机制下就有可能会出现粘包现象,即在发送缓存区中的数据有可能是由几个包和一个不完整的包组成的TCP数据包,当缓冲区被数据填满就会被立即发送.

### UDP
UDP(短链接) 一种面向报文的无连接传输层协议，提供的是不可靠传输协议.UDP正式通信前不会做双方协商确认,不关心数据传输状态,只管发包,收包,不做校验.

> 正是由于UDP协议不关心网络传输等一系列状况,使得UDP协议在数据传输过程中节省大量的网络状态确认和数据校验的系统资源消耗,大大提升了UDP的传输效率,传输速度明显快于TCP.

为什么不考虑TCP做音视频传输?
> TCP是面向连接的,可靠的传输协议,所以在连接建立前会做双方的协商确认,在发送数据是会做类似签名的过程,收包时会做包校验,在发送失败是时还会做超时重传.以上这些机制加上流量控制机制还有频繁的确认校验过程会使得音视频的接受效率大大降低.音视频注重的时即时性,TCP的特性决定了音视频的即时性注定无法与UDP相比.

音视频传输特点
> 1.传输时延要求小,实时性要求高.

> 2.传输流量大,要求传输效率高

> 3.在一定范围内允许丢包或是传输错误.

所以UDP更理想.

## 操作系统
### 大端机、小端机
小端模式(Little-endian)[当下最常见]
> 数据低字节保存在内存低地址,数据高字节保存在内存的高地址中.大端模式则刚好相反.

大端模式(Big-endian)
> 数据的高字节保存在内存的低地址,低字节保存在内存的高地址中.


### 大端字节序与小端字节序
> 计算机硬件有两种储存数据的方式：大端字节序（big endian）和小端字节序（little endian）.

###　操作系统中进程调度策略有哪几种？
> 先来先服务、优先级、时间片轮转、多级反馈.

### 进程和多线程
进程
> 进程是具有一定独立功能的程序关于某个数据集合上的一次运行活动,!!![进程是系统进行资源分配和调度的一个独立单位]!!!.

线程
> 线程是进程的一个实体,是CPU调度和分派的基本单位,它是比进程更小的能独立运行的基本单位.线程自己基本上不拥有系统资源,只拥有一点在运行中必不可少的资源(如程序计数器,一组寄存器和栈),但是它可与同属一个进程的其他的线程共享进程所拥有的全部资源. 

进程和多线程共享些什么?

代码段、进程当前前的目录、进程用户ID、组ID、信号处理器.

线程独有:

1.线程ID. 2.寄存器组的值. 3.线程占用的堆栈. 4.线程的信号屏蔽码. 5.线程优先级.

区别
> 二者主要去别在与是否拥有独立空间,进程有,线程没有.进程可以创建和撤销线程,反过来却不可以.

> 进程之间不会相互影响(故障隔离特性!),一个线程挂掉会导致整个进程挂掉.

关系
> 一个线程可以创建和撤销另一个线程;同一个进程中的多个线程之间可以并发执行.
### 进程的内存布局
由低地址到高地址:
> 保留区 -> 代码和只读数据区(代码、字符串常量、宏定义) -> 数据段(全局变量、静态变量、初始化数据段、未初始化数据段) ->　堆区(低地址往高地址扩展//自下往上)-> 未使用空间 -> 文件映射区(动态库,共享内存) -> 未使用空间 -> 栈区(高地址往低地址扩展//自上往下) -> 内核区

保留区 -> 代码和只读区(代码、字符串常量、宏定义) -> 数据段(.bbs->.data) -> 堆区 ->为占用空间 -> 文件映射区 -> 为占用空间 -> 栈区 -> 内核区

.bbs 段(未赋初值)
> 定义但为赋初值的 全局变量、静态变量、常量

.data 段(已赋初值)
> ...

####　用户存储空间的角度看内存布局

代码区、文字常量区、动态存储区、静态存储区

> 动态存储区: 栈(函数返回地址、参数、局部变量、auto 声明的变量--其实也是非静态变量)和堆(new malloc alloc...).

> 静态存储区(存储和程序生命周期一样的变量): 全局变量、静态变量.

> 字节序 : 小端存小端 大端相反 字节序关乎值表示.
