VMWare12密钥：5A02H-AU243-TZJ49-GTC7K-3C61N

#### 常用操作

设置root密码`sudo passwd root`

修改时区

```sh
tzselect
sudo ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
```

在当前目录查找某个字符串 `grep str *`，在当前目录下递归查找字符串`grep -r str ./`

新建文档 `touch filename`

编辑文档 `nano/vim/gedit filename`

重命名或移动 `mv oldpath newpath`

删除目录 `rm -rf dir_path` 

编译 `g++ test.cpp -o test`

目录生成树状图 `tree`

修改文件权限为用户级`chmod 777 filename`

编辑环境变量`nano /etc/profile`，使生效`source /etc/profile`

查看80端口信息`netstat -ntulp |grep 80`

换下载源`nano /etc/apt/sources.list`



#### Ubuntu18没有上网图标

```shell
sudo service network-manager stop
sudo rm /var/lib/NetworkManager/NetworkManager.state
sudo service network-manager start

sudo nano /etc/NetworkManager/NetworkManager.conf
把false改成true
```

#### ifconfig发现没有eth0网卡

```sh
sudo ifconfig eth0 up
sudo dhclient eth0
```

如果没有IP地址，关闭

#### WSL环境下安装Ubuntu

WSL：Windows Subsystem for Linux，不用装VMWare

https://www.computerhope.com/issues/ch001879.htm#install


