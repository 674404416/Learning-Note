# extern "C"是什么以及如何实现的

> 参考自https://blog.csdn.net/qq_24282081/article/details/87530239

### 1.extern “C”是什么

在c++中用c语言的方式编译

### 2.如何实现的

在编译一个函数后，实际的函数名会改变(多态)。

这时，如果在c++里面调用c里面实现的函数就会报错（找不到）。

这是为什么呢？

因为改变的规则在c和c++里面是不一样的

c中是在函数名前面加上一个_,如add变成 _add

而c++更为复杂

![img](https://img-blog.csdnimg.cn/2019021714002222.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzI0MjgyMDgx,size_16,color_FFFFFF,t_70)

所以如果想在c++里面调用c里面的函数

就要在c文件中加上extern "C"

