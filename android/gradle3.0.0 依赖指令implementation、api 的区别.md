### api 指令
完全等同于compile指令，没区别，你将所有的compile改成api，完全没有错。

### implementation指令
这个指令的特点就是，对于使用了该命令编译的依赖，对该项目有依赖的项目将无法访问到使用该命令编译的依赖中的任何程序，也就是将该依赖隐藏在内部，而不对外部公开。

简单的说，就是使用implementation指令的依赖不会传递。例如，有一个module为testsdk，testsdk依赖于gson：

`implementation 'com.google.code.gson:gson:2.8.2'`

这时候，在testsdk里边的java代码是可以访问gson的。

另一个module为app，app依赖于testsdk：

`implementation project(':testsdk')`

这时候，因为testsdk使用的是implementation 指令来依赖gson，所以app里边不能引用gson。

但是，如果testsdk使用的是api来引用gson：

`api 'com.google.code.gson:gson:2.8.2'`

则与gradle3.0.0之前的compile指令的效果完全一样，app的module也可以引用gson。这就是api和implementation的区别。

### 建议
在Google IO 相关话题的中提到了一个建议，就是依赖首先应该设置为implementation的，如果没有错，那就用implementation，如果有错，那么使用api指令。使用implementation会使编译速度有所增快。