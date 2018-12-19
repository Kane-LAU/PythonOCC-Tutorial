# PythonOCC-Tutorial (English Version/中文版)
This tutorial will be used to illustrate the pythonocc with specific examples , and guide the fresh to learn it(from installation to learning basic functions)
The guide will demonstrate the procress in detail so that everyone can follow it without interrupt 
# About PythonOCC 
pythonocc is a python library whose purpose is to provide 3D modeling features. It is intended to developers who aim at developing CAD/PDM/PLM applications. it is developed by [tpaviot](https://github.com/tpaviot), you can check the original source from the channel or repo

# why I write this?
PythonOCC, i think, is a good open source for CAD/CAE/CAM designer. It is very easy to use owing to the characteristics of python.
 we should appreciate Tomes paviot, who provided us the tool to design our products. Unfortunately, it  only provided us excellent tool but  so limited guide(such as installation,basic functions use). so i think the **tutorial** can compensate with the weakeness
 
 
 
 
 
 # PythonOCC教程
本教程会使用具体的例子来去说明pythonocc的使用，会包括基本的安装（非常详尽的说明）和常用函数的使用。
来使用pythonocc，我觉得可能的原因之一就是python的简单易用，如果再让你去读c++版本的opencascade教程，我认为会是一个非常折磨的过程。所以我只专注于在pythonocc里的实现。所以请大胆食用！
# 关于PythonOCC 
pythonOCC是python语言构架的 3D CAD/CAE/PLM开发框架，它提供了如下功能： 复杂曲面的操作，信息转换（STEP,IGES,STL格式），用户界面可视化（基于wxpython库或者qt库），jupyter nootbook生成等。 他是由 [tpaviot](https://github.com/tpaviot)开发并发布的，你可以搜索pythonocc来搜索源代码

# 为什么我写此教程?
我认为PythonOCC是一个非常好的开源资源,对于那种想使用较少的代码实现cad/cae/cam程序的人非常友好 。但是不幸的事实是，目前pythonocc只是在发布，却并没有详尽的教程介绍它，虽然目前开发者更新了example，但是却有些杂乱，没有起到一个系统的教学的目的。该文档将细致地去解析pythonocc，去弥补它的缺点




# 目录/CONTENTS
## 一、pythonocc入门指导   The Introduction to pythonocc
  - [1.1搭建pythonocc的虚拟开发环境](https://github.com/liuxin2322/PythonOCC-Tutorial/blob/master/chinese%20version/simple%20introduction/pythonocc%E5%85%A5%E9%97%A8%E6%8C%87%E5%AF%BC%EF%BC%9A1.%E6%90%AD%E5%BB%BApythonocc%E7%9A%84%E8%99%9A%E6%8B%9F%E5%BC%80%E5%8F%91%E7%8E%AF%E5%A2%83.md)**/**[ Developing virtual environment-pythonocc ]()
  - [1.2 PyCharm连接pythonOCC开发环境，并运行一个简单实例](https://github.com/liuxin2322/PythonOCC-Tutorial/blob/master/chinese%20version/simple%20introduction/pythonocc%E5%85%A5%E9%97%A8%E6%8C%87%E5%AF%BC%EF%BC%9A2.PyCharm%E8%BF%9E%E6%8E%A5pythonOCC%E5%BC%80%E5%8F%91%E7%8E%AF%E5%A2%83%EF%BC%8C%E5%B9%B6%E8%BF%90%E8%A1%8C%E4%B8%80%E4%B8%AA%E7%AE%80%E5%8D%95%E5%AE%9E%E4%BE%8B.md)**/**[ Running simple examples using Pycharm ]()
   - [1.3 创建属于自己的主界面及对话框及安装qtdesigner](https://github.com/liuxin2322/PythonOCC-Tutorial/blob/master/chinese%20version/simple%20introduction/pythonocc%E5%85%A5%E9%97%A8%E6%8C%87%E5%AF%BC%EF%BC%9A3.%E5%88%9B%E5%BB%BA%E5%B1%9E%E4%BA%8E%E8%87%AA%E5%B7%B1%E7%9A%84%E4%B8%BB%E7%95%8C%E9%9D%A2%E5%8F%8A%E5%AF%B9%E8%AF%9D%E6%A1%86%E5%8F%8A%E5%AE%89%E8%A3%85qtdesigner.md)**/**[ Create your GUI with qtdesigner ]()
  - [1.4 使用pyinstaller封装成exe文件](https://github.com/liuxin2322/PythonOCC-Tutorial/blob/master/chinese%20version/simple%20introduction/pythonocc%E5%85%A5%E9%97%A8%E6%8C%87%E5%AF%BC%EF%BC%9A4.%E4%BD%BF%E7%94%A8pyinstaller%E5%B0%81%E8%A3%85%E6%88%90exe%E6%96%87%E4%BB%B6.md)**/**[ Generating exe file using pyinstaller ]()
  
## 二、pythonocc基础使用 The Basic Use to PythonOCC
**2.1 获取物体信息   Obtain obiect information** 

   - [2.1.1 读入iges，step，stl文件]()**/**[ Read iges,step and stl format]()
   - [2.1.2 提取曲线上的点位信息或者曲面上的点位信息]()**/**[ Obtain the point position and normal on curves or surfaces]()
   
 **2.2 显示与交互 Display and interaction** 
 
   - [2.2.1 显示]()**/**[ Display]()
   - [2.2.2 交互]()**/**[ Interaction]()
   
 ## 三、pythonocc函数一览    The glance of the functions with pythonocc
 ## 四、pythonocc常见问题集锦 The issue collection of pythonocc
   - [安装问题]()
   - [其他问题]()
