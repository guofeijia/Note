##  mail

发送和接收电子邮件

- 命令名称：mail。
-  英文原意：send and receive Internet mail。
-  所在路径：/bin/mail。
-  执行权限：所有用户。
-  功能描述：发送和接收电子邮件。

###  发送邮件

```
[root@localhost ~]# mail userl
Subject: hello <-邮件标题
Nice to meet you! <-邮件具体内容
. <-使用.来结束邮件输入
#发送邮件给user1用户
```

我们接收到的邮件都保存在"/var/spod/mail/用户名"中，每个用户都有一个以自己的用户名命名的邮箱。

###  发送文件内容

```
[root@localhost ~]# mail -s "test mail" root </root/ anaconda-ks.cfg
#把/root/anaconda-ks.cfg文件的内容发送给root用户
```

选项：
-s： 指定邮件标题

###  查看接收邮件

```
[root@localhost ~]# mail
Heirloom Mail version 12.4 7/29/08.Type ?for help.
"/var/spool/mail/root": 1 message 1 new
>N 1 root Mon Dec 5 22:45 68/1777 "test mail"<-之前收到的由件
>N 2 root Mon Dec 5 23:08 18/602 "hello"
#未阅读编号发件人 时间 标题
&
<-等待用户输入命令
```

可以看到已经接收到的邮件列表，"N"代表未读邮件，如果是已经阅读过的邮件，则前面是不会有这个"N"的；之后的数字是邮件的编号，我们主要通过这个编号来进行邮件的操作。如餓们想要査看第1邮件，则只需输入邮件的编号"1"就可以了

在交互命令中

- headers：列出邮件标题列表，直接输入"h"命令即可。
-  delete：删除指定邮件。比如想要删除第二封邮件，可以输入"d2"。
-  save：保存邮件。可以把指定邮件保存成文件，如"s 2/tmp/test.mair。
-  quit：退出，并把已经操作过的邮件进行保存。比如移除已删除邮件，保存已阅读邮脾。
-  exit：退出，但是不保存任何操作。

