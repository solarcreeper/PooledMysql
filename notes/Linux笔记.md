# Linux 系统的顶层目录结构
/              根目录  
├── bin     存放用户二进制文件  
├── boot    存放内核引导配置文件  
├── dev     存放设备文件  
├── etc     存放系统配置文件  
├── home    用户主目录  
├── lib     动态共享库  
├── lost+found     文件系统恢复时的恢复文件  
├── media   可卸载存储介质挂载点  
├── mnt     文件系统临时挂载点  
├── opt     附加的应用程序包   
├── proc    系统内存的映射目录，提供内核与进程信息  
├── root    root 用户主目录  
├── sbin    存放系统二进制文件  
├── srv     存放服务相关数据  
├── sys     sys 虚拟文件系统挂载点  
├── tmp     存放临时文件  
├── usr     存放用户应用程序  
└── var     存放邮件、系统日志等变化文件  

# 修改linux 用戶名為隱藏
打開.bashrc文件
修改 PS1='${debian_chroot:+($debian_chroot)}\u@\h:\w\$ 
為PS1='${debian_chroot:+($debian_chroot)}:\w\$


# 开启端口



