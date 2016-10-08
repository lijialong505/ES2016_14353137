<<<<<<< HEAD
#嵌入式第一次实验报告

###  1. Description
        首先我们要知道什么是DOL，DOL的全名是分层式分布。是一个软件开发框架程序并行的应用程序。
        其中我们需要了解到的我们需要用的一些工具：
        1. make工具
            主要用来工程编译和程序链接。我们会用到makefile文件，用于告诉make使用何种方式来编译运行源代码。make还有一个功能就是可以通过比较文件最后修改的时间决定文件的修改与否。
        2. ant工具
            ant是一种基于Java的build工具。用于自动调用程序完成项目的编译、打包和测试。
        3. JAVA和JAVAC
            JAVAC用于编译java代码，而JAVA可以打开已经编译好的class文件。
###  2.How to install
        1. 安装环境
           $ sudo apt-get update
           $ sudo apt-get install ant
           $ sudo apt-get install openjdk-7-jdk
           $ sudo apt-get install unzip
        2. 下载文件
           $ sudo wget http://www.accellera.org/images/downloads/standards/systemc/systemc-2.3.1.tgz
           $ sudo wget http://www.tik.ee.ethz.ch/~shapes/downloads/dol_ethz.zip
        3.解压文件
           $ mkdir dol
           $ unzip dol_ethz.zip -d dol
           $ tar -zxvf systemc-2.3.1.tgz
        4.编译systemc
           $ cd systemc-2.3.1
           $ mkdir objdir
           $ cd objdir
           $ ../configure CXX=g++ --disable-async-updates
           $ sudo make install
           $ pwd
        5.编译dol
           property name=”systemc.inc” value=”YYY/include”（修改编译的systemc位置）
           property name=”systemc.lib” value=”YYY/lib-linux/libsystemc.a”/
           $ ant -f build_zip.xml all
           $ cd build/bin/main
           $ ant -f runexample.xml -Dnumber=1

最后结果:           
![Paste_Image.png](http://upload-images.jianshu.io/upload_images/3162604-62c6484c40638da7.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


###  3.Experimental experience
      基本上每次实验都是从配置环境开始的，配置环境首先是为以后的实验打好基础，也是让我们了解实验的基本原理是什么。
      这次实验配置也是遇到了很多问题，并且是配置了两次（第一次失败了.....） 第二次也是最后创建失败，让TA大大帮忙看了之后发现是需要加一个sudo增加权限，真是醉了。
=======
# ES2016_14353137
>>>>>>> 7adc467b0a8250c1470370b2c459219b442c2bcf
