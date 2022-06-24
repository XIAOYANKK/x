# 参考资料
先丢两篇cmake资料，这两篇算是写的比较精简囊括挺多东西的两篇。第一篇包括cmake基本简介与语法，第二篇是对新增包的具体操作。\
[1.简介、语法、简单操作](https://blog.csdn.net/geyichongchujianghu/article/details/124781090?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522165573447616780357223340%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=165573447616780357223340&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduend~default-1-124781090-null-null.142^v18^control,157^v15^new_3&utm_term=cmake%E8%AF%AD%E6%B3%95%E8%AF%A6%E8%A7%A3&spm=1018.2226.3001.4187)
\
[2.添加包](https://blog.csdn.net/zhanghm1995/article/details/105466372?spm=1001.2101.3001.6650.1&utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-1-105466372-blog-123942764.pc_relevant_antiscanv3&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-1-105466372-blog-123942764.pc_relevant_antiscanv3&utm_relevant_index=2)
\
第一篇从第11点入手，基本的操作语法不是很复杂，就固定的几个语句，看不懂语句在回溯前面的语法。
\
第二篇可以从示例入手，主要通过更改主目录下的CMakeLists.txt中的内容以实现。
# 注意
\
**cmake_minimum_required() 命令**
\
对于该命令，语法如下：
```C++
cmake_minimum_required(VERSION <min>[...<max>] [FATAL_ERROR])
```
该命令定义工具版本。CMake 工具版本太旧的话，可能 CMakeLists.txt 使用了新的语法，就会不兼容；CMake 工具版本太新的话，也会出现不兼容问题，因为 CMake 新版本在更新时 不一定向后兼容，CMake 老版本的一些功能可能删除、更改。
\
我尝试找opencv包时，所要定义的版本是3.5.5。
\
**对于工程目录的定义**
参照文章1分别建立CMakeLists.txt、main.cpp、sub文件，在sub文件放自定义的库。
\
对于cmake .操作后在主目录生成过多文件问题，可建立build文件夹，进入build文件后，执行cmake ..，其生成的文件将进入build，便于工程管理。
