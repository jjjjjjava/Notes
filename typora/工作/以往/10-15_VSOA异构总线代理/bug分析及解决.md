[toc]

## DoRpcResponse造成内核崩溃

### 问题描述

![image-20231031100529474](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231031100529474.png)

### 问题分析

错误原因：如下图，send中数据param和data是指针类型，需要初始化，不能直接memcpy，否则会产生野指针，访问错误内存地址的现象

![image-20231031100647583](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231031100647583.png)

![img_v2_cffa40ee-2649-4e76-8802-3c3a89f878bg](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\img_v2_cffa40ee-2649-4e76-8802-3c3a89f878bg.jpg)

![image-20231031100623948](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231031100623948.png)

![2750f8e6-9153-4969-b08a-65b26c1a5c11](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\2750f8e6-9153-4969-b08a-65b26c1a5c11.jpeg)



### 解决方法

如下图，不用memcpy，直接赋值即可。

![image-20231031100841118](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231031100841118.png)





## 无法发送不带负载的rpc请求

### 问题描述

无法发送不带负载的rpc请求

### 问题分析

如下图：OnRpcRequestProxy函数中len在没有负载时返回-1。

所以是：-1和sizeof(tmpbuf)做比较，而sizeof返回的是无符号整数。此时：当比较有符号整数和无符号整数时，有符号整数会被隐式转换为无符号整数。

因此-1>sizeof(tmpbuf)

![image-20231031101122357](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231031101122357.png)

![image-20231031101138608](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231031101138608.png)

![image-20231031101145674](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231031101145674.png)

