### 0.前言
pythonOCC也就是opencascade的python封装版本，是由tpaviot制作并发行的。[这里是tpaviot制作者Github的主页](https://github.com/tpaviot)
**pythonocc简介：**
原文：
pythonOCC is a 3D CAD/CAE/PLM development framework for the Python programming language. It provides features such as advanced topological and geometrical operations, data exchange (STEP, IGES, STL import/export), GUI based visualization (wx, Qt), jupyter notebook rendering.
译文：pythonOCC是python语言构架的 3D CAD/CAE/PLM开发框架，它提供了如下功能： 复杂曲面的操作，信息转换（STEP,IGES,STL格式），用户界面可视化（基于wxpython库或者qt库），jupyter nootbook生成等。

### 1.所需材料
         

 - anaconda
Anaconda指的是一个开源的Python发行版本，其包含了conda、Python等180多个科学包及其依赖项。 使用anaconda配置环境，则可以免去相当多的手动配置烦恼。
可以在这里进行下载安装包：[anaconda下载地址](https://www.anaconda.com/download/)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20181117140207870.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80Mjc1NTM4NA==,size_16,color_FFFFFF,t_70)
 ###  2.**创建**
 目前在网上pythonocc环境创建的信息非常少，而且都还停留在0.17版本，并且例子非常有限。这也是为什么我写此教程的原因，毕竟这条路我走的太艰难，**希望后来者可以顺畅一些**。
 **注意**以下代码均在anaconda prompt运行，切记！！
 ![](https://img-blog.csdnimg.cn/20181117140036443.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80Mjc1NTM4NA==,size_16,color_FFFFFF,t_70)
 
**可以成功创建的代码如下**
```
conda create -n pythonocc -c conda-forge -c dlr-sc -c pythonocc -c oce pythonocc-core==0.18.1 python=3.6
```
上面的代码的含义是：
`conda create -n pythonocc` 代表在anaconda 的环境下创建一个虚拟环境，名字为pythonocc，这个虚拟环境在anaconda 的 envs文件夹下，如果成功安装后可以找到这个文件夹
![在这里插入图片描述](https://img-blog.csdnimg.cn/20181211234912799.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80Mjc1NTM4NA==,size_16,color_FFFFFF,t_70)
则可以发现，相关的安装包则会被列举出来，这些是需要下载的东西，输入y（表示同意下载并自行安装），下载时间比较长，请耐心等待

3.**激活环境**
输入`activate pythonocc` 则可以进入pythonocc环境（这一步用于检验是否下载和搭建成功，当然还有其他作用，这里不再赘述）
![在这里插入图片描述](https://img-blog.csdnimg.cn/20181117140416209.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80Mjc1NTM4NA==,size_16,color_FFFFFF,t_70)

如果你在实际创建过程中出现任何问题，请随时联系我，如果我了解，一定会尽量帮你解决
QQ：1185753125

 

***下一篇***：[**第一个pythonocc程序**](https://blog.csdn.net/weixin_42755384/article/details/84187356)
***如果你遇到了问题，请在这里寻找答案***：[**pythonocc常见问题集锦**](https://blog.csdn.net/weixin_42755384/article/details/84187626)
