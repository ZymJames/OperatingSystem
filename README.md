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
简单动画的生成<br>
![](https://github.com/ZymJames/OperatingSystem/blob/master/cartoon.jpg)<br>
计算器（输入简单的加减乘除运算式，可以得出结果）<br>
![](https://github.com/ZymJames/OperatingSystem/blob/master/calculator.png)<br>
扫雷小游戏（生成不同难度的扫雷地图，玩法规则与经典扫雷相同）<br>
![](https://github.com/ZymJames/OperatingSystem/blob/master/mine.png)<br>
心得体会<br>
经过本次项目，我们对操作系统之于计算机的作用有了更直观的认识，实际上操作系统也是一个程序，但它是能够直接管理和控制计算机硬件与软件资源的最基本的系统软件，其他软件的运行，需要操作系统提供接口，而用户使用计算机，也需要操作系统提供接口。在这一次应用程序的编写中，我们就学习到，操作系统是如何先将机器语言转换成汇编语言，再用汇编语言生成了一系列库函数以供高级语言调用并编写程序，而编写好程序后，还要将程序写入磁盘扇区，才能最终进入文件系统供用户使用。从前我们一直疑惑为什么C语言能跑出这样那样的效果呢，这些高级语言为什么编写结束后就生成了一个文件，然后我们点击这个文件就能跑程序了呢。而在对操作系统有了更深入的理论学习和实践后，我们的疑惑多少得到了解答。<br>
组员分钟<br>
王思源：在文件系统中写入可执行文件，应用程序的编写<br>
占毅鸣：应用程序的编写，资料文档的收集整理<br>
分数分配：50%—50%


