#rip实验的配置
##
###网络拓扑图：


![](http://i.imgur.com/4VZqZdA.png)


##


####什么是rip?
**rip**  **如图，R0只知道192.168.78.0以及另一段的192.168.78.4和它相连的两个网段，**
**但是，对于R1,R2而言，路由器不知道这些网段的存在，因此，需要一个协议来告诉其他路由器这些网段的存在，而rip就是这个作用，将R0的路由表同时转发到其他的路由器上，这样，几个路由器都知道这些网段的存在了。**

###路由器关于rip的配置如下：
    router rip

    network  net [wildmask]

###上面的两个命令行，一个是开启rip模式，如果想要关闭就在rip前面加上No
    eg. no network
###network的意思就是将自己的路由表告知其他的路由器，这些网段的存在。
###其实rip的作用就相当于一个存储命令行的云，接收后就将这些网段告知其他的路由器；



####实验结果：
>最后我还是在这个rip的实验中ping通了。