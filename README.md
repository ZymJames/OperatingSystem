# OperatingSystem
操作系统课程项目<br>
小组成员：王思源1552678，占毅鸣1552679<br>
所在班级：2班<br>
Git托管地址：https://github.com/ZymJames/OperatingSystem<br>
项目说明：<br>
    本项目在操作系统中编写了应用程序，通过调用操作系统当前的进程映像，从硬盘上读取一个可执行文件，而这个可执行文件就是我们编写的应用程序，从而在源码上实现用户级的应用。<br>
    在具体的实现过程中，由于操作系统源码已经准备了若干可用于应用程序的库函数，所以我们就将这些库函数单独链接成一个文件，换句话说就是聚合了一个C运行时库，而这个库里面编译好了应用程序在运行中需要的所有库函数代码。其中特殊的是，main() 函数作为整个应用程序运行的主函数，需要操作系统专门为其准备参数（argc和argv），并进行调用，才能让应用程序跑起来，在main()函数运行时，再逐个编译程序的代码，让应用程序发挥其作用。<br>
    而在应用程序的代码编写完成后，还需要将其安装到源码的文件系统中。此时我们要做的就是为应用程序编译链接，然后将编译好的应用程序打成tar包，再写入磁盘映像的扇区中，启动系统后，将tar包解压到文件系统中，这样就能把写好的应用程序放到文件中，供用户使用。<br>
这次我们写的应用程序有如下几个：<br>

![简单动画的生成](https://github.com/ZymJames/OperatingSystem/blob/master/cartoon.jpg)
