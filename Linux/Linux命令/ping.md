##  ping

ping 是常用的网络命令，主要通过 ICMP 协议进行网络探测，测试网络中主机的通信情况。

- 命令名称：ping。
-  英文原意：send ICMP ECHO_REQUEST to network hosts。
-  所在路径：/bin/ping。
-  执行权限：所有用户。
-  功能描述：向网络主机发送 ICMP 请求。

###  命令格式

```
[root@localhost ~]# ping [选项] IP
```

选项： 

-  -b: 后面加入广播地址，用于对整个网段进行探测；
-  -c 次数： 用于指定 ping 的次数；
-  -s 字节： 指定探测包的大小；

 