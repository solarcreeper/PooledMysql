# 网站目录是否可见    
## 在配置虚拟机目录中：    
 Options Indexes FollowSymLinks # Indexes 表示这个网站可以显示结构目录, 要关闭的话去掉Indexes即可.

## apache web 文件无法进行读写
  对应目录进行授权
  例如：需要在/home/log下创建日志文件
  将该目录加入到apahe默认用户组www-data中
  ```shell
  cd /home
  sudo chgrp -R www-data log
  sudo chmod -R g+w log
  ``` 