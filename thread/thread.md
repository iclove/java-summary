## 多线程
- 线程定义、线程周期
- 线程和进程的区别
- 多线程的好处
- 实现多线程
- 多线程的使用

由于计算机基础偏弱，底层系统原理基本为零，因此对于进程调度和多线程实现原理一概不知。在通过google、blog、书籍等方式整理总结产出本文，希望能够为漫漫无期的coder修行之路点亮一栈明灯，照我前行😆

### 资源说
自从冯诺依曼开辟计算机结构模型，计算机系统被抽象成 CPU + 存储器 + IO，故得由上古大神定义，这里勉强将计算机资源定义为

* 计算机资源
* 存储资源

#### 概念定义
- 临界区：
每个进程中访问临界资源的那段代码称为临界区（Critical Section）（临界资源是一次仅允许一个进程使用的共享资源）。 每次只准许一个进程进入临界区，进入后不允许其他进程进入。 不论是硬件临界资源，还是软件临界资源，多个进程必须互斥地对它进行访问。 多个进程中涉及到同一个临界资源的临界区称为相关临界区。
- 原子性：
即一个操作或者多个操作 要么全部执行并且执行的过程不会被任何因素打断，要么就都不执行。
- 可见性：
指当多个线程访问同一个变量时，一个线程修改了这个变量的值，其他线程能够立即看得到修改的值。
- 有序性：
即程序执行的顺序按照代码的先后顺序执行。



#### CPU
而著称计算机大脑的CPU是计算机单元，对coders来说，它是黑盒的。它只对输入的指令和数据进行计算，然后输出结果，它不负责管理计算哪些“指令和数据”。换言之，CPU同志只提供计算能力，不负责分配计算资源。

计算机资源是由操作系统（调度模块）分配的，是由操作系统按照一定的规则来分配什么时候由谁来获得CPU上的计算资源，比如[时间片](https://zh.wikipedia.org/wiki/%E6%97%B6%E9%97%B4%E7%89%87)。






