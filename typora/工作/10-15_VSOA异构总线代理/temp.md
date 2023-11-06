[toc]

## 服务端打印信息

root@sylixos:/apps/proxy/bin]# ./proxy
home_path=/apps/proxy
config_path=/apps/proxy/config
F 18:28:24. 6 INFO   (proxy:src/server/proxy.cpp:57) - position->Start() success.
F 18:28:24. 6 INFO   (proxy:src/server/position_task.cpp:156) - server Position is starting...
F 18:28:24. 6 INFO   (proxy:src/server/proxy.cpp:63) - proxy_task->Start() success.
F 18:28:24. 6 INFO   (proxy:src/server/proxy_task.cpp:567) - ProxyTask service start...
F 18:28:24. 6 INFO   (proxy:src/server/cfgm.cpp:49) - GetLocalServerList in file /apps/proxy/config/config.json.
F 18:28:24. 6 INFO   (proxy:src/server/cfgm.cpp:234) - start ConfigModel::GetProxyBusInfo read file:/apps/proxy/config/config.json.
F 18:28:24. 6 INFO   (proxy:src/server/cfgm.cpp:100) - read no.0 local_server success:server=a2_server, host=127.0.0.1, port=3333
F 18:28:24. 6 INFO   (proxy:src/server/cfgm.cpp:272) - proxy_bus type is .
F 18:28:24. 6 INFO   (proxy:src/server/position_task.cpp:57) - get local server number is:1
F 18:28:24. 6 INFO   (proxy:src/server/proxy_task.cpp:470) - connect param is port=/dev/ttyS0;baudrate=115200;parity=0;databits=8;stopbits=1
F 18:28:24. 6 INFO   (proxy:src/server/cfgm.cpp:145) - start GetProxyServerList from /apps/proxy/config/config.json.
set serial parommunicateInitConn: set param success
F 18:28:24. 6 INFO   (proxy:src/server/cfgm.cpp:189) - read no.0 proxy_server success:server=a1_server, port=10001, station_no=0
F 18:28:24. 6 INFO   (proxy:src/server/proxy_task.cpp:476) - CommunicateInitConn port=/dev/ttyS0;baudrate=115200;parity=0;databits=8;stopbits=1 success
CheckAndConnect: open /dev/ttyS0 success
CheckAndConnect: control /dev/ttyS0 success
F 18:28:24. 6 INFO   (proxy:src/server/position_task.cpp:84) - get proxy server number is:1
F 18:28:24. 6 INFO   (proxy:src/server/proxy_task.cpp:483) - CommunicateConnect s

F 18:28:24. 6 INFO   (proxy:src/server/position_task.cpp:112) - position seuccess, conn_param=port=/dev/ttyS0;baudrate=115200;parity=0;databitsrver information: ip=127.0.0.1, port=3000.
=8;stopbits=1
F 18:28:33. 6 INFO   (proxy:src/server/cfgm.cpp:145) - start GetProxyServerList from /apps/proxy/config/config.json.
F 18:28:33. 6 INFO   (proxy:src/server/cfgm.cpp:189) - read no.0 proxy_server success:server=a1_server, port=10001, station_no=0
F 18:28:33. 6 INFO   (proxy:src/server/proxy_task.cpp:490) - ProxyTask::OnStart(), GetProxyServerList size 1.
F 18:28:33. 6 INFO   (proxy:src/server/position_task.cpp:125) - VSOA position server start success
F 18:28:33. 6 INFO   (proxy:src/server/proxy_task.cpp:498) - ProxyTask::OnStart(): start session a1_server success.
F 18:28:33. 6 INFO   (proxy:src/server/position_task.cpp:164) - server position in event loop, bstop = 0
F 18:28:33. 6 INFO   (proxy:src/server/cfgm.cpp:49) - GetLocalServerList in file /apps/proxy/config/config.json.
F 18:28:33. 6 INFO   (proxy:src/server/cfgm.cpp:100) - read no.0 local_server success:server=a2_server, host=127.0.0.1, port=3333
F 18:28:33. 6 INFO   (proxy:src/server/proxy_task.cpp:506) - ProxyTask::OnStart(), GetLocalServerList size 1.
F 18:28:33. 6 INFO   (proxy:src/server/proxy_session.cpp:44) - ProxySession, create proxy session:{"name":"a1_server"} success, port=10001
F 18:28:33. 6 INFO   (proxy:src/server/proxy_session.cpp:55) - Added listener for server:a1_server with URL:/
F 18:28:33. 6 INFO   (proxy:src/server/proxy_session.cpp:65) - Started vsoa server:a1_server with address:127.0.0.1 and port:10001
F 18:28:33. 6 INFO   (proxy:src/server/client_session.cpp:48) - OnStart: start client sessiont to server:a2_server success
F 18:28:33. 6 INFO   (proxy:src/server/proxy_task.cpp:513) - ProxyTask::OnStart(): start client session of a2_server success.
F 18:28:33. 6 INFO   (proxy:src/server/proxy_task.cpp:526) - start echo timer success, timeval=20s
F 18:28:33. 6 INFO   (proxy:src/server/proxy_task.cpp:42) - last time heart beat recv is :1970-1-1 08:00:00
F 18:28:33. 6 INFO   (proxy:src/server/proxy_task.cpp:52) - timeout to get heart beat from peer
~~Q���F 18:28:33. 6 INFO   (proxy:src/server/proxy_task.cpp:90) - handle_timeout: send heart beat success
F 18:28:34. 6 WARN   (proxy:src/server/proxy_task.cpp:992) - msg is shorter than a smallest package.
F 18:28:34. 6 WARN   (proxy:src/server/proxy_task.cpp:639) - ParseRecvMessage get a package failed.
F 18:28:37. 6 WARN   (proxy:src/server/proxy_task.cpp:992) - msg is shorter than a smallest package.
F 18:28:37. 6 WARN   (proxy:src/server/proxy_task.cpp:639) - ParseRecvMessage get a package failed.
F 18:28:39. 6 WARN   (proxy:src/server/proxy_task.cpp:992) - msg is shorter than a smallest package.
F 18:28:39. 6 WARN   (proxy:src/server/proxy_task.cpp:639) - ParseRecvMessage get a package failed.
timeout to recv from serial port:/dev/ttyS0, timeout is: 3000 ms
timeout to recv from serial port:/dev/ttyS0, timeout is: 3000 ms
timeout to recv from serial port:/dev/ttyS0, timeout is: 3000 ms
F 18:28:53. 6 INFO   (proxy:src/server/proxy_task.cpp:42) - last time heart beat recv is :1970-1-1 08:00:00
F 18:28:53. 6 INFO   (proxy:src/server/proxy_task.cpp:52) - timeout to get heart beat from peer
~~e���F 18:28:53. 6 INFO   (proxy:src/server/proxy_task.cpp:90) - handle_timeout: send heart beat success
timeout to recv from serial port:/dev/ttyS0, timeout is: 3000 ms
timeout to recv from serial port:/dev/ttyS0, timeout is: 3000 ms
timeout to recv from serial port:/dev/ttyS0, timeout is: 3000 ms
timeout to recv from serial port:/dev/ttyS0, timeout is: 3000 ms
timeout to recv from serial port:/dev/ttyS0, timeout is: 3000 ms







## 可行性分析

首先有两块

1. 任务卡和地面站

   1. 3DR Radio传输，受限物理介质，数据量不用考虑

   ![image-20231025095639962](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231025095639962.png)

   2. 主要考虑WIFI情况，当WIFI连接时，对数据量的要求就起来了，数据量=每次发送数据*频率，频率肯定有所降低，还会增加负载。

2. 任务卡和飞控卡

   1. usb，负责升级，这个不是实时性要求的，因此不重要。
   2. 通信串口，正常情况，飞控只需要发送主要的数据，因此数据量的传输不是很重要。关键是及时性问题。但是目前反映，飞控自身处理飞行控制，任务卡只需发送大致指令，不需要时刻做出安排

3. 关键：

负载，要去实验，然后做负载实验，线程池+很多个请求，去看它的cpu负载怎么样。

第一，程序能搞起来绝对不简单，它线程池他那边没有实现，它缺少了一个函数，我虽然能把这个函数覆写，但是我要把整个都给搞起来是很难的

第二，









负载，数据量，频率（发送间隔），及时性



负载：要经过测试

数据量：单个*频率，单个发送的数据是一样的，频率肯定有所减少。考虑和飞控要求不高，所以暂不考虑。地面站：射频不考虑，wifi要考虑。

频率：肯定有所降低，

及时性：对及时性的要求。





## 测试步骤

1. 迁移云原生
2. 设置IP，串口。
3. 通过IDE的Terminal进行控制





## 位置服务

位置服务要配置环境变量

![image-20231026173543724](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231026173543724.png)

1. 配置位置服务的地址与端口号。通过配置环境变量的方式进行配置，并执行varsave命令保存配置。

   ```bash
   [root@sylixos:/root]# VSOA_POS_SERVER=127.0.0.1:3000
   [root@sylixos:/root]# varsave
   ```





192.168.128.18

![image-20231027143108411](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231027143108411.png)

![image-20231027143115511](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231027143115511.png)

![image-20231027143200385](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231027143200385.png)

![image-20231027143846805](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231027143846805.png)

![image-20231027143954261](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231027143954261.png)

## 显示成功的结果![image-20231027170115771](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231027170115771.png)



![3118d2c6-e84d-41a4-b4cf-4cb242871ca4](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\3118d2c6-e84d-41a4-b4cf-4cb242871ca4-1698397281677-2.jpeg)

![image-20231027170644165](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231027170644165.png)

![image-20231027180524135](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231027180524135.png)



## 报错信息

![img_v2_283e25a7-a1aa-4a42-833c-cc45f333d88g](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\img_v2_283e25a7-a1aa-4a42-833c-cc45f333d88g.jpg)

F 01:05:00. 1 INFO   (proxy:src/server/proxy_task.cpp:654) - recv a message, code=3, payload={"src":"A1","dst":0,"seqno":0,"code":0,"message":"success","payload":{"param":"eyJsaWdodCI6IDF9\n","data":"eyJsaWdodCI6IDF9\n"}}
F 01:05:00. 1 INFAPI_SemaphoreMPend() error: semaphore handle invalidate.
in thread 4000036[pthread] proc 2[/apps/proxy/bin/proxy] context.
API_SemaphoreMPend() error: semaphore handle invalidate.
in thread 4000036[pthread] proc 2[/apps/proxy/bin/proxy] context.
API_SemaphoreMPend() error: semaphore handle invalidate.
in thread 4000036[pthread] proc 2[/apps/proxy/bin/proxy] context.





![image-20231027180417497](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231027180417497.png)



![image-20231028152036182](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231028152036182.png)

![image-20231028152049854](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231028152049854.png)

recv a message, code=3, payload={"src":"A1","dst":1,"seqno":15,"code":0,"message":"success","payload":{"param":"eyJsaWdodCI6IDF9\n","data":"eyJsaWdodCI6IDF9\n"}}

![image-20231028151843944](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231028151843944.png)



测试时间：15:35-

![image-20231028153602128](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231028153602128.png)





http://www.baidu.com/light

vsoa://A1/light



![image-20231028162738643](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231028162738643.png)

![image-20231028163111889](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231028163111889.png)







出现多个同名线程

![image-20231028163501383](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231028163501383.png)

是不是因为您这里面new太多啊？





![image-20231028173024218](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231028173024218.png)









今天初步解决问题

![img_v2_47895b51-0872-4d1e-8962-d891cd4fa08g](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\img_v2_47895b51-0872-4d1e-8962-d891cd4fa08g.jpg)





## 服务端错误

![image-20231030172204813](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231030172204813.png)

![image-20231030172217353](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231030172217353.png)

![image-20231031170549641](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231031170549641.png)

### 猜测一：while循环中

### 猜测二：接收线程缓冲区爆了，导致无法接收

添加打印数据：  zlog_info(proxy_cat, "\n\nproxy->cur_recvbuf_length = %d\n\n", proxy->data_len);

**排除**

### 猜测二：rpc_client这一侧的代理服务端的A1死掉了

rpc_client这一侧的代理服务端的A1死掉了

![image-20231101135741501](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231101135741501.png)



![image-20231101135752031](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231101135752031.png)

错误，它只是转化为了RpcRequestSend_Thread线程

### 猜测四：锁的问题，有进程死锁了

![image-20231101163418754](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231101163418754.png

![image-20231101164056199](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231101164056199.png)

![image-20231101182241106](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231101182241106.png)

### 解决:实际是串口发送函数的问题

**问题如下图：**

![9881ac9a-6a94-45fd-b2d9-3f8c08068998](C:\Users\jjjjjjava\AppData\Roaming\LarkShell\OptimizeImage\9881ac9a-6a94-45fd-b2d9-3f8c08068998.jpeg)





**修改后测试**：

起始时间

![image-20231102174556898](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231102174556898.png)

截止时间

![image-20231102175759812](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231102175759812.png)



重新开始

![image-20231102175805708](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231102175805708.png)

哥，假设有拼包现象。那么就是发送的一个包被分成两个包。那就是三块，第一块接收12，第二块接收0，第三块接收5。

按照您的循环来，

第一次是接收到了12，然后他不是一个完整的包，然后您进行解析，发现解析失败，无法进行处理

第二次接收到0，然后您continue。

第三次接收到5，此时从您传递的recvbuf的位置并不是上次接收到的位置+1，而是起始位置，所以同第一次。



那是不是可以通过在您这里加一个记录当前缓冲区位置的指针进行优化呢？





![image-20231103093537591](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231103093537591.png)







**系统功能结构设计**

**组件级别：**

- 空中平台1
  - 包含：飞控机、任务卡、无人机接口 APP、无人机控制 APP
- 空中平台2
  - 包含：飞控机、任务卡、无人机接口 APP、无人机控制 APP
- 地面电脑
  - 包含：Windows 操作系统、SylixOS、EdgeOS、地面 APP



**组件详细功能**

**无人机接口 APP**

- 目的：实现空中平台1与地面电脑的通信和数据交互。

- 功能：

  - 与任务卡1串口连接。
  - 转发 MAVLINK 消息至地面 APP。
  - 接收来自地面 APP 的 MAVLINK 消息。
  - 解码 MAVLINK 消息，提取无人机信息。
  - 广播“飞行状态消息”。

  

**地面 APP**

- 目的：接收无人机数据，显示在界面上，控制任务，实现空地通信。

- 功能：

  - 从无人机接口 APP1 和 APP2 接收 MAVLINK 消息并透传到UDP端口。
  - 具备图形用户界面，显示多个无人机的“飞行状态消息”。
  - 在地图上显示无人机图标。
  - 具备网页服务器功能，展示界面信息在连接到电脑的浏览器上。
  - 发送“任务指令消息”给无人机控制 APP1 和 APP2。

  

**无人机控制 APP**

- 目的：接收“飞行状态消息”和“任务指令消息”并处理。
- 功能：
  - 接收“飞行状态消息”包括本机和其他无人机的信息。
  - 计算生成“控制指令消息”。
  - 发送“控制指令消息”给无人机接口 APP1。
  - 具备接收“任务指令消息”的能力。





**功能模块**

1. **通信模块**：
   - 无人机接口 APP1
   - 无人机接口 APP2
   - 地面 APP
2. **数据处理模块**：
   - 无人机接口 APP1
   - 无人机接口 APP2
   - 地面 APP
3. **控制模块**：
   - 无人机控制 APP1
   - 无人机控制 APP2
   - 地面 APP
4. **显示模块**：
   - 地面 APP

![image-20231103170351367](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231103170351367.png)

控制层



uint8_t



![image-20231106100453149](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231106100453149.png)

![image-20231106100310083](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231106100310083.png)

Software Is Expired, Please Contact The Publisher (ACOINFO)!
API_SemaphoreMPend() error: called from ISR.
in interrupt contex.
API_SemaphoreMPost() error: called from ISR.
in interrupt contex.
API_SemaphoreMPend() error: called from ISR.
in interrupt contex.
API_SemaphoreMPost() error: called from ISR.
in interrupt contex.
API_SemaphoreMPend() error: called from ISR.
in interrupt contex.
in interrupt context system low memory.
_IoOpen() error: file can not create
in interrupt contex.



![image-20231106100635120](C:\Users\jjjjjjava\Nutstore\1\我的坚果云\typora\typora-pic\image-20231106100635120.png)

哥，您好，目前来说可以一直保持连接了，我从周五早上10:30，一直跑到19:30，直到因为其它原因才结束，总计9个小时，总计收发34571个。

在您的指导和协助下，解决和克服了很多问题，最终让它稳定且无误的跑了起来。

接下来就是在这个框架的基础上面开发应用程序和其他架构。

一切准备就绪且无误后，就能够实现您这个框架的真正的实用价值了，让它真正绽放出它的光芒了，您之前的苦心也不会白费。
