# mysql5.7 修改用户初始密码的方法

## 修改用户的初始化密码:

``` sql
SET PASSWORD = PASSWORD(‘your new password');
ALTER USER ‘root'@‘localhost' PASSWORD EXPIRE NEVER;
flush privileges;
```
## 创建新的用户:
``` sql
CREATE USER ‘username'@‘host' IDENTIFIED BY ‘password';
```
##给用户授予权限:

``` sql
GRANT all privileges ON databasename.tablename TO ‘username'@‘host';
flush privileges;
```

## 设置和更改密码：

```sql
SET PASSWORD FOR ‘username'@‘host' = PASSWORD(‘password');
```

## 撤销权限：

``` sql 
REVOKE privilege ON databasename.tablename FROM ‘username'@‘host';
```
## 删除用户:

``` sql
DROP USER ‘username'@‘host';
```
## 查看用户的授权:
```sql
SHOW grants for ‘username'@‘host';
```