# 远程登陆

1.修改 /etc/mysql/mhysql. conf.d/mysqld.cnf，注释 bind -address = 127.0.0.1  
2.登陆mysql,对指定账户进行远程登陆授权
```shell
grant all privileges on *.* to root@'%' identified by 'meiyoumima'
```
3.重启mysql
4.maybe 需要增加3306端口的防火墙设置