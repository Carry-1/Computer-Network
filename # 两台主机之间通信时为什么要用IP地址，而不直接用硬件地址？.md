# 两台主机之间通信时为什么要用IP地址，而不直接用硬件地址？
&emsp;&emsp;既然在网络链路上传送的数据帧最终是用硬件地址来寻找目的主机，为什么还要用IP地址进行通信，为什么不直接是用硬件地址进行通信？   
&emsp;&emsp;首先要知道，在全世界有各种各样的网络（如WAN，LAN，2G，3G），它们使用不同的硬件地址，要使这些异构网络进行通信必须要进行硬件地址转换，而要让用户或者用户主机来完成这一任务几乎是不可能的（虽然我也不知道为什么这项工作很复杂），但采用IP编址之后，全球的每台主机似乎都处于同一个网络之中，它们都拥有唯一的一个IP地址，它们的通信似乎就像连接在同一个网络上一样方便。两台主机通信时，只需知道对方的IP地址即可，因为复杂的IP地址到硬件地址的转换是由通过软件调用ARP来实现的。

# 参考文献   《计算机网络》 谢希仁