# Openpose
## 行为识别

# Openpose Windows安装

###################################################################

**！！！！！！！！！！！！！！！！！！trick：步骤2 和 步骤3 不想做的话，直接从网盘下载后进行第4步就行**

链接：https://pan.baidu.com/s/1E7gKSlF-dXP3hMsDdNnIHA 
提取码：1111 

###################################################################
## 1. 准备工作

> 1. Git 已经安装
> 2. CUDA及Cudnn
> 3. VS2017（其他也可以）
> 4. Cmake（下载的时候从官网找mis的安装包）



## 2. 下载cource code

官网下载地址：

https://github.com/CMU-Perceptual-Computing-Lab/openpose/releases   （哪个顺眼下载哪个）



解压后在主目录下创建build文件夹

## 3. 下载各个需要的包，大概7-8个，放到指定位置

参考：

 https://blog.csdn.net/zb1165048017/article/details/82115724/



## 4. Cmake工作

> 1. 打开Cmake
> 2. source code 选择主目录， binaries选择主目录下的bulid
> 3. 点击configure，弹出的窗口第一行选择自己的VS版本，第二行选择**X64**，不选的话默认32位，会失败
> 4. configure成功后主体大部分为红色，此时再次点击configure红色消失
> 5. 点击generate生成openpose.sln



## 5. VS下的操作

> 1. 打开build下的openpose.sln， 看解决方案配置及解决方案平台是否位realease及X64，如果是就对了，不是的话调成这个
> 2. 右键解决方案然后点“生成解决方案”，不报错的话就完成了所有操作。
> 3. 从解决方案资源管理器找到03的小demo，右键设置为启动项，运行成功即完成。



## 6. 采坑点

> 1. Cmake编译的时候报git错，就是git装完还没重启电脑
> 2. Cmake编译的时候遇到个错误忘了，发现是我把BULID_PYTHON给勾上了，其实目前用不上的，勾上就报了缺少啥东西的错误。
> 3. 报运行预测程序的时候VSRUNTIME_1D.DLL缺少，说明Cmake的时候没选择X64，或方案配置选择的debug导致的
