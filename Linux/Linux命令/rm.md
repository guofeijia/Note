##  rm

rm 是强大的删除命令，不仅可以删除文件，也可以删除目录

* 命令名称：rm
*  英文原意：remove files or directories。
*  所在路径：/bin/rm。
*  执行权限：所有用户。
*  功能描述：删除文件或目录。

###  命令格式

``` 
[root@localhost ~]# rm[选项] 文件或目录
```

选项： 

-  -f：强制删除（force）
-  -i：交互删除，在删除之前会询问用户
-  -r：递归删除，可以删除目录（recursive）

###   例子

```
[root@localhost ~]# mkdir -p /test/lm/movie/jp/
#重新建立测试目录
[root@localhost ~]# rm -rf/test/
#强制删除，一了百了
```

