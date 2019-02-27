##  netstat

网络状态查看命令，既可以查看本机开启的端口，也可以查看哪些客户端连接

- 命令名称：netstat。
-  英文原意：Print network connections, routing tables, interface statistics, masquerade connections, and multicast memberships。
-  所在路径：/bin/netstat.
-  执行权限：所有用户。
-  功能描述：输出网络连接、路由表、接口统计、伪装连接和组播成员。

 ###  命令格式

```
[root@localhost ~]# netstat [选项]
```

选项： 

-  -a：列出所有网络状态，包括 Socket 程序；
-  -c秒数：指定每隔几秒刷新一次网络状态；
-  -n：使用 IP 地址和端口号显示，不使用域名与服务名；
-  -p：显示 PID 和程序名；
-  -t：显示使用 TCP 协议端口的连接状况；
-  -u：显示使用 UDP 协议端口的连接状况；
-  -I：仅显示监听状态的连接；
-  -r：显示路由表；