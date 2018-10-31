### vps搭建owncloud

[owncloud官方一键包合集](https://download.owncloud.org/download/repositories/stable/owncloud/)

命令行：
```
Run the following shell commands as root to trust the repository.

rpm --import https://download.owncloud.org/download/repositories/production/CentOS_7/repodata/repomd.xml.key
Run the following shell commands as root to add the repository and install from there.

wget http://download.owncloud.org/download/repositories/production/CentOS_7/ce:stable.repo -O /etc/yum.repos.d/ce:stable.repo
yum clean all
yum install owncloud-files
```

完成后重启apache：

`service httpd start`

加入开机自动启动apache

chkconfig httpd on

查看服务运行状态

`systemctl status httpd.service`

安装php环境

cenos自带的php是5.4，owncloud必须是5.6  开始装个7.0也不行

卸载自带php

`yum remove php-common`

然后安装5.6

`yum install -y php56w php56w-opcache php56w-xml php56w-mcrypt php56w-gd php56w-devel php56w-mysql php56w-intl php56w-mbstring`