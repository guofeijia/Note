##  chown

修改文件和目录的所有者和所属组

- 命令名称：chown。
-  文原意：change file owner and group。
-  所在路径：/bin/chown。
-  执行权限：所有用户。
-  功能描述：修改文件和目录的所有者和所属组。

###  命令格式

```
[root@localhost ~]# chown [选项] 所有者：所属组 文件或目录
```

选项：-R  递归设置权限，也就是给子目录中的所有文件设置权限

```
[root@localhost ~]# touch laowang
#由root用户创建laowang文件
[root@localhost ~]# ll laowang
-rw-r--r-- 1root root 0 6月 16 05:12 laowang
#文件的所有者是root，普通用户user对这个文件拥有只读权限
[root@localhost ~]# chown user laowang
#修改文件的所有者
[root@localhost ~]# ll laowang
-rw-r--r-- 1 userroot 0 6月 16 05:12 laowang
#所有者变成了user用户，这时user用户对这个文件就拥有了读、写权限
```

```
[root@localhost ~]# chown user:user laowang
# ":"之前是文件的所有者，之后是所属组。这里的":"也可以使用"."代替
[root@localhost ~]# ll laowang
-rw-r--r-- 1 user user 0 6月 16 05:12 laowang
```

注意：超级用户可以修改任何文件的权限，普通用户只能修改自己文件的权限。也就是说，只有普通用户是这个文件的所有者，才可以修改文件的权限。