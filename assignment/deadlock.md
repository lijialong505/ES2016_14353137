##1.实验内容
      本次内容是让我们实现一种操作系统中会出现的一种现象——死锁。
      我们已知死锁会产生的条件：
      1.互斥条件  2.请求与保持条件  3.不剥夺条件  4.循环等待
      条件。然后就是想办法建立一个可以产生死锁的程序。
##2.实验步骤
      1.首先建立两个线程。然后保证每个线程都会实现一个功能例如输出的动作。
         然后使用synchronize修饰该线程的代码块。（synchronize的功能是
         能够保证在同一时刻最多只有一个线程访问该段代码）
      2.接着建立会产生死锁的程序，生成一个java文件。然后建立一个令程序跑
         1000次的bat程序。运行得出结果。
##3.实验原理
          因为有synchronize的存在，保证了last这个函数只可以在同一时间
       被一个线程使用，如果有两个线程同时使用到了这个函数，就会发生死锁现
       象。而我们在代码中可以发现，A对象会使用B中的last函数，而B对象同时
       会使用A中的last函数。然后看死锁函数，其中A会在延迟count的时间之后
       运行。而B也会执行。
          如果只运行几次的话，可以说产生死锁的概率并不是很大，但是一旦运行
       次数增多，就很可能会出现A和B在同一时刻共用last函数的情况产生死锁。
##4.实验结果截图
![建立A和B两个线程](http://upload-images.jianshu.io/upload_images/3162604-b54c50df7e6b5edb.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![建立会产生死锁的程序](http://upload-images.jianshu.io/upload_images/3162604-f9680893135a172c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


![停在了第28次的时候，产生了死锁](http://upload-images.jianshu.io/upload_images/3162604-d537ba066aa563d4.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

