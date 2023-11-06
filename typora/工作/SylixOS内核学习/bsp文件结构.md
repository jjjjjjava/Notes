[toc]

## 概览

一个标准的BSP文件，其工程目录如下：

![image-20230927150112282](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20230927150112282.png)

SylixOS BSP文件结构主要包含以下四个部分：

Include为代表的头文件，SylixOS中的文件，config.h为代表的配置，链接文件，以及编译后生成的debug或release文件

## Include

Includes 文件主要包含 BSP 工程在编译 BASE 和编译工具链中需要用到的头文件，如下图所示

![image-20230927150716091](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20230927150716091.png)

上面的两个.h文件夹是编译工具链中需要用到的头文件

下面的ECS开头的是编译BASE中需要用到的头文件

## SylixOS文件

该文件中包含bsp工程中的主要程序和代码，主要由三个子文件夹组成，如下图所示

![image-20230927151041849](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20230927151041849.png)

- bsp文件夹中主要包含系统启动的程序代码，包括：汇编代码，内存映射，BSP参数配置等。整个 BSP 工程编译完之后，此文件夹内还会生成 symbol.c 和symbol.h 两个包含符号表的文件
- driver文件夹中主要包含整个操作系统运行时需要用到的底层硬件的驱动代码。	
- user 文件夹里面只有一个文件 main.c，整个 main.c 里只有一个接口，用于在操作系统系统成功启动之后，创建出一个 tshell 终端。



## config配置文件

主要是用于对整个工程编译和链接的配置

-  config.h 用于配置系统的 ROM，RAM 等参数。

![image-20230927153635893](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20230927153635893.png)

- config.mk，Makefile，myBsp.mk 用于编译 BSP 工程。 

config.mk

![image-20230927153903242](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20230927153903242.png)

- config.ld，SylixOSBSP.ld 用于链接 BSP 工程。

#### SylixOSBSP.ld值得一看。

## Debug或Release文件

整个 BSP 工程编译完成之后，还会自动生成另外一个文件夹。工程如果是 debug模式，则会生成一个 Debug 文件夹；反之，其模式是 release 模式，则会生成一个Release 文件夹。生成的这个文件夹包含编译完成最终生成的 elf 文件和 bin 文件

什么是elf和bin文件？