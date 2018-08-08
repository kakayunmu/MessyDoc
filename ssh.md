# 服务器维护常用命令

## 链接远程服务器

``` shell
ssh root@47.105.120.227
```
## 上传
- ### 上传文件到服务器

``` shell
scp /path/filename username@servername:/path   

```
- ### 上传目录到服务器
``` shell
scp  -r local_dir username@servername:remote_dir
```

## 下载
- ### 从服务器上下载文件

``` shell
scp username@servername:/path/filename /var/www/local_dir（本地目录）
```
- ### 从服务器下载整个目录
``` shell
scp -r username@servername:/var/www/remote_dir/（远程目录） /var/www/local_dir（本地目录）
```

## 运行 jar

``` shell
java -jar xxx.jar 
```

### 后台运行 jar
``` shell
nohup java -jar bluebox-1.0-SNAPSHOT.jar --spring.application.profiles.active=prd > 1.log 2>&1 &
```

### 查看某端口占用的线程的pid
``` shell
netstat -nlp |grep :8080
```