##  locate

只能按照文件名来进行搜索

- 命令名称：locate。
-  英文原意：find files by name。
-  所在路径：/usr/bin/locate。
-  执行权限：所有用户。
-  功能描述：按照文件名搜索文件。

###  命令格式

```
[root@localhost ~]# locate [选项] 文件名
```

选项-i：忽略大小写

### 注意：

+  新建的文件无法铜鼓locate命令查找，这是因为 locate 命令不会直接搜索硬盘空间，而会搜索 locate 数据库。这样做的好处是耗费系统资源小、搜索速度快；缺点是不是实时更新的，而要等用户退出登录或重启系统时，locate 数据库才会更新，所以我们无法查找到新建立的文件

​       locate命令的数据库在：/var/lib/mlocate/mlocate.db

​       如果我们不想退出登录或重启系统，则也可以通过 updatedb 命令来手工更新这个数据



* 新建立了 /tmp/lmls 文件，而且也执行了 updatedb 命令，却依然无法找到这个文件，这就要来看看 located 配置文件 /etc/updatedb.conf了

  在 locate 执行搜索时，系统认为某些文件系统、某些文件类型和某些目录是没有搜索必要的,比如光盘、网盘、临时目录等，这些内容要么不在 Linux 系统中，是外来存储和网络存储，要么是系统的缓存和临时文件。刚好 /tmp/ 目录也在 locate 搜索的排除目录当中，所以在 /tmp/ 目录下新建的文件是无法被找到的