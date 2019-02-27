##  ifconfig

linux中查看和临时修改IP地址的命令，centos7中使用指令  ip a  查看IP地址配置

- 命令名称：ifconfig。
-  英文原意：configure a network interface。
-  所在路径：/sbin/ifconfig。
-  执行权限：超级用户。
-  功能描述：配置网络接口。

###  查看IP地址

```
[root@localhost ~]# ifconfig
```

###  临时配置IP地址

```
[root@localhost ~]#ifconfig eth0 192.168.44.3
#配置IP地址，不指定子网掩码就会使用标准子网掩码
[root@localhost ~]#ifconfig eth0 192.168.44.3 netmask 255.255.255.0
#配置IP地址，同时配置子网掩码
```

