网络通讯命令
============

命令列表
--------

|命令|简介|
|----|----|
|telnet|基于telnet协议，与其它计算机通信|
|ssh|基于OpenSSH协议的远程登录客户端|
|scp|基于OpenSSH协议的安全复制远程文件|
|ftp、sftp|文件传输工具|
|ifconfig|配置网络接口|
|netstat|查看网络状态|
|tcpdump|网络传输数据分析工具|
|ping|查看主机是否可到达|
|whois|域名查询工具|
|talk|与其他在线用户交流|
|write|向其他在线用户发送消息|
|wall|向所有在线用户发消息|


telnet：基于telnet协议，于其他计算机通信
----------------------------------------
* 常用执行方式：`telnet hostname/ip [port]`
* 说明：
	* 如果端口未指定，采用默认端口：23
	* telnet是明文传输，所以对于密码等数据不安全
	* 连接主机后，进入命令模式：ctrl+]

ssh：远程登录到指定的主机
-------------------------
* 常用执行方式：
	* `ssh -l login-name hostname/ip [port]`
	* `ssh login-name@hostname/ip [port]`
* 说明：
	* 默认端口22
	* ssh是加密传输

scp：基于OpenSSH协议的安全复制远程文件
--------------------------------------
* 执行方式：
	* 本机-`>`远程：scp local-files loginname@remote-host/ip:[dir/file]
	* 远程主机-`>`本机：scp login-name@remote-host/ip:files local-dir
* 常用选项：
	* -p：保持文件权限
	* -r：递归式复制

ftp：基于ftp协议的文件传输客户端
--------------------------------
* 常用执行方式：ftp [options] hostname/ip
* 常用选项：
	* -i：关闭多问间传输过程中的交互式确认动作
* 常用命令：    

|命令|描述|命令|描述|
|----|----|----|----|
|ascii|文本传输模式|binary(bin)|二进制传输模式|
|bye|退出ftp命令|cd、lcd|切换远程、本地目录|
|cdup|远程切换到上一级目录|chmod|同linux chmod|
|delete|删除文件|get、mget|下载单个、多个文件|
|ls、lls|列举远程、本地文件|put、mput|上传单个、多个文件|
|rename|重命名远程文件|rmdir|删除远程目录|

ifconfig：配置网络接口
----------------------
* 通常运行方式：
	* 查看网络接口信息：`ifconfig [-a|-s] [interfaces]`
	* 设置网络接口(需root权限)：ifconfig interface ip
* 常用选项：
	* -a：查看所有可用网络接口的信息
	* -s：简短模式
	* up、down：启用、禁用网络接口

netstat：查看网络状态
---------------------
* 说明：此命令用来显示网络连接，路由表，接口状态，伪装连接，网络链路信息和组播成员组等
* 常用选项：
	* -a：所有侦听或不在侦听的socket状态
	* -c：每秒刷新一次统计输出结果
	* -e：附加信息，使用2次获取更详细的信息
	* -n：数字形式的主机名
	* -p：显示socket所属的进程ID和进程名
	* -t：只查看tcp协议的socket
	* -u：只查看udp协议的socket
	* delay：一个整数，按指定的时间间隔刷新统计输出结果

whois：域名查询工具
-------------------
执行方式：whois domain

talk：与其他在线用户交谈
------------------------
* 执行方式：talk user [tty]
* 说明：
	* 要使用talk，系统中必须开启talk服务
	* 可以使用write命令替代talk，write不需配置系统服务

write：向其他在线用户发送消息
-----------------------------
* 执行方式：write user [tty]

wall：向所有在线用户发送消息
----------------------------
* 执行方式：
	* wall
	* wall files



