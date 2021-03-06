##  Linux读写执行权限

###  权限对文件的作用

- -读(r)：对文件有读（r）权限，代表可以读取文件中的数据。如果把权限对应到命令上，那么一旦对文件有读（r）权限，就可以对文件执行 cat、more、less、head、tail 等文件查看命令。
-  -写(w)：对文件有写（w）权限，代表可以修改文件中的数据。如果把权限对应到命令上，那么一旦对文件有写（w）权限，就可以对文件执行 [vi](http://c.biancheng.net/vi/)m、echo 等修改文件数据的命令。注意，对文件有写权限，是不能删除文件本身的，只能修改文件中的数据。如果要想删除文件，则需要对文件的上级目录拥有写权限。
-  -执行(x)：对文件有执行（x）权限，代表文件拥有了执行权限，可以运行。在 [Linux](http://c.biancheng.net/linux_tutorial/) 中，只要文件有执行（x）权限，这个文件就是执行文件了。只是这个文件到底能不能正确执行，不仅需要执行（x）权限，还要看文件中的代码是不是正确的语言代码。对文件来说，执行（x）权限是最高权限。

###  权限对目录的作用

- -读(r)：对目录有读 （r）权限，代表可以查看目录下的内容，也就是可以查看目录下有哪些子文件和子目录。如果把权限对应到命令上，那么一旦对目录拥有了读（r）权限，就可以在目录下执行 ls 命令，查看目录下的内容了。
-  -写(w)：对目录有写（r）权限，代表可以修改目录下的数据，也就是可以在目录中新建、删除、复制、剪切子文件或子目录。如果把权限对应到命令上，那么一旦对目录拥有了写（w）权限，就可以在目录下执行 touch、rm、cp、mv 命令。对目录来说，写（w）权限是最高权限。
-  -执行(x)：目录是不能运行的，那么对目录拥有执行（x）权限，代表可以进入目录。如果把权限对应到命令上，那么一旦对目录拥有了执行（x）权限，就可以对目录执行 cd 命令，进入目录。

### 注意：

目录的可用权限分以下几种：

- 0：任何权都不赋予。
-  5：基本的目录浏览和进入权限。
-  7：完全权限。

对文件有写权限，却不能删除文件

