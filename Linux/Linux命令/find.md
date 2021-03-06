##  find

find 是 [Linux](http://c.biancheng.net/linux_tutorial/) 中强大的搜索命令，不仅可以按照文件名搜索文件，还可以按照权限、大小、时间、inode 号等来搜索文件。但是 find 命令是直接在硬盘中进行搜索的，如果指定的搜索范围过大，find命令就会消耗较大的系统资源，导致服务器压力过大。所以，在使用 find 命令搜索时，不要指定过大的搜索范围。

find 命令是完全匹配的，必须和搜索关键字一模一样才会列出。

- 命令名称：find。
-  英文原意：search for files in a directory hierarchy.
-  所在路径：/bin/find。
-  执行权限：所有用户。
-  功能描述：在目录中查找文件。

###  命令格式

```
[root@localhost ~]# find 搜索路径 [选项] 搜索内容
```

find 是比较特殊的命令，它有两个参数： 

-  第一个参数用来指定搜索路径；
-  第二个参数用来指定搜索内容。

###  按文件名搜索

```
[root@localhost ~]#find 搜索路径 [选项] 搜索内容
```

选项： 

-  -name: 按照文件名搜索；
-  -iname: 按照文件名搜索，不区分文件名大小；
-  -inum: 按照 inode 号搜索；

###  按照文件大小搜索

```
[root@localhost ~]#find 搜索路径 [选项] 搜索内容
```

选项： 

-  -size[+-]大小：按照指定大小搜索文件，"+"的意思是搜索比指定大小还要大的文件，"-" 的意思是搜索比指定大小还要小的文件，千字节必须是小写的"k"，而兆字节必领是大写的"M"，

  'c' for bytes  搜索单位是c，按照字节搜索

  'w' for two-byte words

  #搜索单位是w，按照双字节（中文）搜索

  'k'for Kilobytes (units of 1024 bytes)

  #按照KB单位搜索，必须是小写的k

  'M' for Megabytes (units of 1048576 bytes)

  #按照MB单位搜索，必须是大写的M

  'G' for Gigabytes (units of 1073741824 bytes)

  #按照GB单位搜索，必须是大写的G

###  按照修改时间搜索

```
[root@localhost ~]# find搜索路径 [选项] 搜索内容
```

选项：

-  -atime [+-]时间: 按照文件访问时间搜索
-  -mtime [+-]时间: 按照数据修改时间搜索
-  -ctime [+-]时间: 按照状态修改时间搜索

 这三个时间的区别我们在 stat 命令中已经解释过了，这里用 mtime 数据修改时间来举例，重点说说 "[+-]"时间的含义。 

-  -5：代表前5天内修改的文件（1-5）。
-  5：代表前5~6天那一天修改的文件（5-6）。
-  +5：代表6天前修改的文件（>6）。

###  按照权限搜索

```
[root@localhost ~]# find 搜索路径 [选项] 搜索内容
```

选项：

-  -perm 权限模式：査找文件权限刚好等于"权限模式"的文件
-  -perm -权限模式：査找文件权限全部包含"权限模式"的文件
-  -perm +权限模式：査找文件权限包含"权限模式"的任意一个权限的文件

 ###  按照所有者和所属组搜索

```
[root@localhost ~]# find 搜索路径 [选项] 搜索内容
```

选项：

-  -uid 用户 ID:按照用户 ID 査找所有者是指定 ID 的文件
-  -gid 组 ID:按照用户组 ID 査找所属组是指定 ID 的文件
-  -user 用户名：按照用户名査找所有者是指定用户的文件
-  -group 组名：按照组名査找所属组是指定用户组的文件
-  -nouser：査找没有所有者的文件

 ###  按照文件类型搜索

```
[root@localhost ~]# find 搜索路径 [选项] 搜索内容
```

选项:

-  -type d：查找目录
-  -type f：查找普通文件
-  -type l：查找软链接文件

###  逻辑运算符

```
[root@localhost ~]#find 搜索路径 [选项] 搜索内容
```

选项： 

-  -a：and逻辑与
-  -o：or逻辑或
-  -not：not逻辑非