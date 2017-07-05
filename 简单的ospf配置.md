#关于ospf的简单配置

##
网络拓扑图如下：
![](http://i.imgur.com/c11YPOz.png)


###明白什么是ospf？


>ospf是Open Shortest Path First开放式最短路径优先的简称；

>一种链路状态协议；

###如何配置ospf？

*其实这个协议在这个网络拓扑图中起到的作用就是向其他的路由宣告其路由表，有这些网段，因此，最关键的就是打开路由的ospf功能；*


###路由器配置如下


		en  //先进入用户模式
		config t //进入配置模式
		interface gi0/0    ///进入路由端口
		ip address xxx.xxx.xxx.xxx  mask  //配置端口ip
		no shutdown  //打开端口
		exit  //退出端口
###ospf的配置：


>en 

>interface loopback 1  //给路由器设置一个路由Id

>ip address xxx.xxx.xxx.xxx mask  //给路由器id的设置一个ip地址

>exit  //退出端口


>router ospf 进程号

>network xxx.xxx.xxx.xxx [wildmask] area [number]

>exit  //退出端口