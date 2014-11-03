常用Linux命令——打包备份
=======================

tar：UNIX打包工具
-----------------
* 执行方式：`tar action [options] [files]`
* 常用操作(操作前的 - 可要可不用)：
	* [-]c:创建
	* [-]t:查看tarfile里面的文件
	* [-]x:解包
* 常用选项：
	* -C：指定路径
	* -f：执行文件名称
	* -j：操作bzip2格式的文件
	* -p：操作过程中保持各文件的原有的权限
	* -v：操作过程中显示文件
	* -z：操作gzip格式的文件
* 示例：

```Shell
#将指定的一个或多个文件、目录内容打成tar包，并查看打包过程，保留文件权限
$ tar -cvpf first.tar tree *.sql linux_cmd/*
$ 											 
#将上述文件、目录打成tar包，并用gzip格式压缩
$ tar -czpf first.tar.gz tree *.sql linux_cmd/*
$ 
#用bzip2格式压缩
$ tar -cjpf first.tar.bz2 tree *.sql linux_cmd/*
$ 
#利用tar复制
$ tar -cvf -/etc | tar -xvf -
$ 
#解包tar
$ tar -xvpf first.tar

