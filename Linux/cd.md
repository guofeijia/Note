##		cd

cd是切换所在目录的命令，是shell内置命令

* 命令名称：cd。
*  英文原意：change directory。
*  所在路径：[Shell](http://c.biancheng.net/shell/) 内置命令。
*  执行权限：所有用户。
*  功能描述：切换所在目录。

###		命令格式

```
[root@localhost ~]#cd [目录名]
```

cd 命令是非常简单的命令，仅有的两个选项 -P 和 -L 的作用非常有限，很少使用： 

-  -P（大写）是指如果切换的目录是软链接目录，则进入其原始的物理目录，而不是进入软链接目录；
-  -L（大写）是指如果切换的目录是软链接目录，则直接进入软链接目录。
