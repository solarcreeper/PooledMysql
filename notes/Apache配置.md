# Apache
## 安裝

```shell
sudo apt-get install apache2
```
裝好后，配置文件位於/etc/apache2 ,默認網站目錄/var/www/;錯誤日志目錄/var/log/apache2/error.log

## 啓動
```shell
sudo /etc/init.d/apache2 start   || sudo service apache2 start
```

## 重啓

```shell
sudo /etc/init.d/apache2 restart || sudo service apache2 restart
```

## 停止

```shell
sudo /etc/init.d/apache2 stop || audo service apache2 stop
```

## 查看版本
```shell
apachectl -v
```

## 配置文件

配置文件路径：/etc/apache2/

```config
# Include module configuration:
Include /etc/apache2/mods-enabled/*.load
Include /etc/apache2/mods-enabled/*.conf

# Include all the user configurations:
Include /etc/apache2/httpd.conf

# Include ports listing
Include /etc/apache2/ports.conf
……
# Include generic snippets of statements
Include /etc/apache2/conf.d/
# Include the virtual host configurations:
Include /etc/apache2/sites-enabled/
```
site-availible存放正真的配置文件，site-enabled存放指向配置文件的符號鏈接(软连接)。
创建一个虚拟机目录，设置工作的网站目录  
DocumentRoot /home/workspace/WebDocumentRoot/

## 创建软连接

```shell
ln -s oldfile newfilelink
```

# 问题

## 访问出现403  
官方文档说明 http://httpd.apache.org/docs/2.4/upgrading.html#access
```document
In 2.2, access control based on client hostname, IP address, and other characteristics of client requests was done using the directives Order, Allow, Deny, and Satisfy.
In 2.4, such access control is done in the same way as other authorization checks, using the new module mod_authz_host
version 2.2 config:

Order allow,deny
Allow from all
version 2.4 config;

Required all granted
```
根据说明，查看本地安装的apache版本为2.4
需要配置虚拟机时使用相应的配置


# PHP

## 安装

```shell
sudo apt-get install php
sudo apt-get install libapache2-mod-php7.0
sudo a2enmod php7.0
```

## 检查
web目录下创建phpinfo.php文件
内容：
```php
<?php
phpinfo();
?>
```
```shell
curl localhost:8080/phpinfo.php
```

## 安装其他php模块


# MYSQL

## 安装

```shell
sudo apt-get install mysql-server
```

# PHPMYADMIN

## 安装
```shell
sudo apt-get install 
Include /etc/phpmyadmin/apache.conf
```


## apache服务器配置端口后外网无法访问：
1.curl localhost：port 检查本地服务是否正常
2.检查服务器防火墙
