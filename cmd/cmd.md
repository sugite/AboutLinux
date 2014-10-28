Linux常用命令
=============

命令的格式
----------
一般Linux命令的格式   
* command [-options] [arguments]
	* 通常一个命令会有（也可以没有）选项和参数
	* 多个选项可以连写，也可以分开
* 一些通用的选项
	* -f：强制执行
	* -h：human readable
	* -i：开启交互模式
	* -r：递归执行

历史命令
--------
* 通过history或fc命令查看之前n个执行过的命令
* !n 
* !cmd：调用历史命令cmd
* 向上箭头键：提取上次命令
```Shell
	$ history   
	......    
	  493 cat /etc/passwd  #493是命令历史号   
	......
	$ !493				#重新执行 cat /etc/passwd   
	$ !ca    #如果之前没有执行过其他以ca开头的命令，则同上   
```


