### 最新cenos執行service httpd restart 報錯Failed to restart httpd.service: Unit not found.
没有默认安装Apache
需要执行`$ sudo yum install httpd`进行安装

设置服务器启动时就开启 Apache 服务
`$ sudo systemctl enable httpd.service`

验证 Apache 服务是否在服务器启动时自动开启了
`$ sudo systemctl is-enabled httpd.service`

如果你看到了这样的响应：

enabled

则说明 Apache 服务已经配置为在服务器启动时自动开启了。

在服务器上启动 Apache 服务的命令为：

`$sudo systemctl start httpd.service`

重新启动 Apache：

`$sudo systemctl restart httpd.service`

停止 Apache：

`$sudo systemctl stop httpd.service`

如果你的服务器正在运行防火墙，请运行下列命令以允许它进行 HTTP 和 HTTPS 通信：

`$sudo firewall-cmd --permanent --zone=public --add-service=http`

`$sudo firewall-cmd --permanent --zone=public --add-service=https`

`$sudo firewall-cmd --reload`

