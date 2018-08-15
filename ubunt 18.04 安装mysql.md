如果 你是 sudo apt install mysql-server

那么 安装 过程中 不会 提示  输入密码  ，然后 你就 坑爹 了  。



 可能的  解决 方案 sudo vim /etc/mysql/debian.cnf  
``` sql
update mysql.user set authentication_string=password('password') where user='root'and Host = 'localhost';
```

 反正这个 办法  我  是 没有 解决  ，搞了 我 两天  也没搞好。草泥马



为了 不用 再次 百度  卸载  mysql 的 命令 如下 

``` shell
sudo apt purge mysql-*
sudo rm -rf /etc/mysql/ /var/lib/mysql
sudo apt autoremove
sudo apt autoreclean

```

解决方案 

https://dev.mysql.com/downloads/file/?id=477124

点击 最下边 download

``` shell
sudo dpkg -i mysql-apt-config_0.8.6-1_all.deb
```

tab 选 ok

``` shell
sudo apt-get update

sudo apt-get install mysql-server 

......
```

过程 中 输入 密码  

大功告成 