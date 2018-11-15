>step 1 : `adb devices`查看手机是否连接成功

>step 2 : `adb tcpip [port]`让手机的某个端口处于监听状态,端口后的范围为5555-5585的奇数端口,默认从5555开始
返回restarting in TCP mode port : 5555代表端口已经处于了监听状态

>step 3 : `adb tcpip [port]`让手机的某个端口处于监听状态,端口后的范围为5555-5585的奇数端口,默认从5555开始
返回restarting in TCP mode port : 5555代表端口已经处于了监听状态

>step 4 : 在手机的wifi设置中查看你的ip地址[ip-address],
使用命令行`adb connect [ip-address]：[port-num]`连接手机,adb connect 手机的ip地址：上面配置的端口号,
返回connected to [ip-address]：[port-num]表示成功连接了手机，现在可以通过wifi在发布调试程序了