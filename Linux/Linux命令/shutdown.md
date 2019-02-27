##  shutdown

关机和重启

- 命令名称：shutdown。
-  英文原意：bring the system down。
-  所在路径：/sbin/shutdown。
-  执行权限：超级用户。
-  功能描述：关机和重启

###  命令格式

```
[root@localhost ~]# shutdown [选项] 时间 [警告信息]
```

选项: 

-  -c：取消已经执行的 shutdown 命令；
-  -h：关机；
-  -r：重启；

###  其他关机重启命令

* reboot   

  ```
  [root@localhost ~]# reboot
  #重启
  ```

*  halt和poweroff

  ```
  [root@localhost ~】# halt
  #关机
  [root@localhost ~】# poweroff
  #关机
  ```

* init

  ```
  [root@localhost~]# init 0
  #关机，也就是调用系统的 0 级别
  [root@localhost ~】# init 6
  #重启，也就是调用系统的 6 级别
  ```

  