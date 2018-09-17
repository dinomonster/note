### Android5.0(棒棒糖)
1)运行时机制,采用ART.安装时转换为机器语言,成为真正本地应用
2)新推出Material Design,用户切换Activity时候无缝过渡位移动画
3)通知详情可以用户自己设计
官网：https://developer.android.com/about/versions/lollipop.html
### Android6.0(棉花糖)
1)运行时权限
2)使用Builder模式来构建通知
3)取消了Apache HTTP客户端
4)低耗电模式,设备处于空闲状态,推迟cpu和网络活动
5)密钥库变更,不在支持DSA,但是依旧支持ECDSA.
6)相机Camera变更为Camera2.之前是先到先得,现在是按照优先级别使用.
官网：https://developer.android.com/about/versions/marshmallow/index.html

### Android7.0(牛轧糖)
1)多窗口支持
2)增强通知功能，如直接回复
3)JIT/AOT编译(Just In Time,Ahead Of Time)
4)随时随地的低耗电,关闭屏幕一段时间就会限制cpu和网络活动
5)快速设置
6)号码屏蔽
7)来电过滤
8)签名V2
官网：https://developer.android.com/about/versions/nougat/android-7.0.html


针对以上，面试中必须记住的是：
1)5.0推出的ART虚拟机，在5.0之前都是Dalvik。他们的区别是：
Dalvik,每次运行,字节码都需要通过即时编译器转换成机器码(JIT)。
ART,第一次安装应用的时候,字节码就会预先编译成机器码(AOT)。
2)6.0 运行时权限申请
3)7.0 多窗口支持，V2签名。

