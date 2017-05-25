### JVM常用命令
* Java Code 和 Heap dump
> Java Code 是描述CPU信息的文件，保存JVM各个线程某一时刻的位置状态信息。

> Heap dump 是描述内存信息的文件，保存JVM堆中对象的内存使用情况。

> java code 
* jinfo：  
> 查看JVM配置参数:  jinfo -flags pid 

* jmap：  
jmap -heap pid：堆空间概览
jmap -dump:live,format=b,file=dump.hprof pid 获取堆内存信息文件  
> 详细的堆dump日志，通过jhat或eclipse MAT工具进行分析，查看对象占用空间情况，进而分析内存泄露

* jstack  
-F 当’jstack [-l] pid’没有相应的时候强制打印栈信息  
-l 长列表. 打印关于锁的附加信息,例如属于java.util.concurrent的ownable synchronizers列表.  
-m 打印java和native c/c++框架的所有栈信息.   
> 
