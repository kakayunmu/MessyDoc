#EDAS 常用命令

## 执行 jar

``` shell
java -Dvipserver.server.port=8080 -Dvipserver.register.ip=192.168.1.158 -Dpandora.location=/home/kakayunmu/.gradle/caches/modules-2/files-2.1/com.taobao.pandora/taobao-hsf.sar/dev-SNAPSHOT/a97d7263c3226c6109af6c4b08189552a6aaeac6/taobao-hsf.sar-dev-SNAPSHOT.jar  -jar sc-
```

## 查找运行的 jar 并结束进程

``` shell
ps -ef |grep [需要查询的进程名称]
```

结束进程 
``` shell
 kill -9 [进程号] 
 ```

## maven 将本地包安装到本地 maven库

jar导入本地库 
``` shell
 mvn install:install-file -DgroupId=com.kakayunmu -DartifactId=sqltool -Dversion=1.0-SNAPSHOT -Dfile=sqltool-1.0-SNAPSHOT.jar -Dpackaging=jar
 ```
