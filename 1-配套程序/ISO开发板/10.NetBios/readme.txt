/******************** (C) 2015 野火 版权所有 ***********************************
* 文件名称           : readme.txt
* 作者               : 
* 版本               : 
* 日期               : 2015/01/28
* 描述               : ping功能
********************************************************************************
* 当前的固件仅用于指导客户开发产品时代码的编写，以帮助其节省时间。因此，野火不承
* 担任何直接或间接的客户代码编写过程中造成的损失。
*******************************************************************************/

例程描述
========
通过NetBIOS服务程序，网络设备上的用户程序可以通过自然语言的名字来访问网络设备。如果说TCP/IP是网络设备之间的“语言”，那么NetBIOS名称服务就是网络设备和用户程序的“桥梁”。
这个应用程序主要就是通过netbios协议来实现把一个简单的自然语言和W5500的IP地址一一对应起来。这样我就可以直接通过输入对应的自然语言名字得到W5500的设备信息。
同时，我们也将http server结合在一起，可以在网页中直接输入对应的自然语言名字进入网页。
本应用代码设置 W5500 为W5500的IP地址对应的自认语言名称。

包含文件目录
============
stm32f10x_conf.h     配置库文件
stm32f10x_it.c       中断头文件
stm32f10x_it.h       stm32f10x_it.c的头文件
main.c               主程序


硬件环境
========
这个例程用于野火STM32F103VET6开发板同以太网芯片W5500搭建的应用平台，也可以很方便地
移植到其他平台上。

注意: 
首先通过串口线连接PC和W5500模块；如果W5500模块直接通过网线和PC相连接，需要修改PC的IP为静态IP，且保证和W5500在同一个网段；
如果W5500模块直接连接路由器，则不需要修改。

操作步骤
========
1. 成功编译应用程序，然后通过串口烧录工具或者Jlink把程序烧录到开发板中
2. 打开串口工具并复位开发板，可以看到通过DHCP自动获取的IP地址
3. 在Windows下执行，开始—运行--（键入）cmd，在弹出的dos窗口中输入 ping+空格+ W5500，如果信息匹配成功，可以看到正确的回复信息，		同时串口也会纤细相应的验证信息
4. 打开IE浏览器，输入W5500也可以得到W5500相关的网页信息
******************* (C) 2015 野火 版权所有 *****************************