上一篇：[运行一个实例](https://blog.csdn.net/weixin_42755384/article/details/84187356)
**在实际的项目中，我们想要实现良好的与用户的互动，图形界面是我们不能忽视的部分。接下来的内容，我们会讲到**

***1. 安装图形界面设计工具——QTdesigner*** 
***2.主界面添加菜单栏***
***3.弹出自定义对话框***


## 一、安装QTdesigner
我们安装的pythonocc虚拟环境已经包含了pyqt的相关文件，但是缺少了qtdesigner
qtdesigner也就是可视化的图形界面设计器，可以让你通过简单的拖拉拽实现图形界面的设计（如：主界面，对话框等），具体安装步骤如下：
### 1.下载一个pyqt5-tool.whl文件：
链接：https://pan.baidu.com/s/1V-xdaFbR1R_3xswbQvyfTA 
提取码：5t3z 

将此文件放在anaconda prompt 默认进入的文件夹（比如我的是 C:\Users\Administrator）
### 2.激活工具
然后程序代码（在 anaconda prompt中输入）：

```
activate pythonocc #激活pythonocc环境
```
```
pip install  PyQt5_Tools-5.7.dev1-py3-none-any.whl 在此环境中安装此包
```

![在这里插入图片描述](https://img-blog.csdnimg.cn/2018112320221632.?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80Mjc1NTM4NA==,size_16,color_FFFFFF,t_70)


然后在（我的是在这里）`D:\ProgramData\Anaconda3\envs\pythonocc\Lib\site-packages\PyQt5-tools\designer`
找到qtdesigner![在这里插入图片描述](https://img-blog.csdnimg.cn/20181123202854587.?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80Mjc1NTM4NA==,size_16,color_FFFFFF,t_70)

### 3.在pycharm中添加该工具
打开pycharm，进入externa tool 创建一个新的项目，按照图片中的内容命名即可：
在program选项中找到designer.exe（我的是在`D:\ProgramData\Anaconda3\envs\pythonocc\Lib\site-packages\PyQt5-tools\designer\designer.exe`）
在working directory 输入：`$FileDir$`

然后ok-->apply后，试着运行一下
![在这里插入图片描述](https://img-blog.csdnimg.cn/20181123203446688.?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80Mjc1NTM4NA==,size_16,color_FFFFFF,t_70)


在左侧区域右键，打开qtdesigner


![在这里插入图片描述](https://img-blog.csdnimg.cn/2018112320385759.?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80Mjc1NTM4NA==,size_16,color_FFFFFF,t_70)


出现如下界面则为成功：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20181123204006229.?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80Mjc1NTM4NA==,size_16,color_FFFFFF,t_70)
## 二、主界面添加菜单栏
代码如下：（同时你可以在这里获得代码文件：https://download.csdn.net/download/weixin_42755384/10838771）
```
#主页添加菜单栏，并在子菜单中可以打开文件选择对话框
from OCC.Display.SimpleGui import init_display
from OCC.gp import gp_Pnt
from PyQt5.QtWidgets import QFileDialog

if __name__ == '__main__':
    display, start_display, add_menu, add_function_to_menu = init_display()
    P0=gp_Pnt(0,0,1)
    P1 =gp_Pnt(0, 30, 20)

    menu_name = '打开'
    menu_name2 = '绘制模型'
    add_menu(menu_name)
    add_menu(menu_name2)
    add_function_to_menu(menu_name, QFileDialog.getOpenFileName)
    start_display()
```
效果图如下：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20181209191424697.?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80Mjc1NTM4NA==,size_16,color_FFFFFF,t_70)

## 三、弹出自定义对话框
**（以下程序文件可在该处下载：（有两个文件）https://download.csdn.net/download/weixin_42755384/10838823）**
#### 1.使用pyqtdesigner 设计一个对话框
如（一）中所介绍，从external tool中打开qtdesigner，选择dialog with button 
![在这里插入图片描述](https://img-blog.csdnimg.cn/2018120919195943.?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80Mjc1NTM4NA==,size_16,color_FFFFFF,t_70)
随便设计一个页面
![在这里插入图片描述](https://img-blog.csdnimg.cn/20181209194433801.?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80Mjc1NTM4NA==,size_16,color_FFFFFF,t_70)
设计好后，使用pyuic（此处不详述，可以自行百度）将ui界面转成py程序
mydialog.py
```
# -*- coding: utf-8 -*-

# Form implementation generated from reading ui file 'mydialog.ui'
#
# Created by: PyQt5 UI code generator 5.6
#
# WARNING! All changes made in this file will be lost!

from PyQt5 import QtCore, QtGui, QtWidgets

class Ui_Dialog(object):
    def setupUi(self, Dialog):
        Dialog.setObjectName("Dialog")
        Dialog.resize(400, 300)
        self.buttonBox = QtWidgets.QDialogButtonBox(Dialog)
        self.buttonBox.setGeometry(QtCore.QRect(30, 240, 341, 32))
        self.buttonBox.setOrientation(QtCore.Qt.Horizontal)
        self.buttonBox.setStandardButtons(QtWidgets.QDialogButtonBox.Cancel|QtWidgets.QDialogButtonBox.Ok)
        self.buttonBox.setObjectName("buttonBox")
        self.pushButton = QtWidgets.QPushButton(Dialog)
        self.pushButton.setGeometry(QtCore.QRect(180, 110, 93, 28))
        self.pushButton.setObjectName("pushButton")

        self.retranslateUi(Dialog)
        self.buttonBox.accepted.connect(Dialog.accept)
        self.buttonBox.rejected.connect(Dialog.reject)
        QtCore.QMetaObject.connectSlotsByName(Dialog)

    def retranslateUi(self, Dialog):
        _translate = QtCore.QCoreApplication.translate
        Dialog.setWindowTitle(_translate("Dialog", "Dialog"))
        self.pushButton.setText(_translate("Dialog", "PushButton"))
```
#### 2.主函数（并在主函数中调用自定义对话框）
test2.py
（实现点击一个点弹出自定义对话框）
```
import sys
from OCC.Display.SimpleGui import init_display
from OCC.gp import gp_Pnt
from mydialog import* #调用自定义对话框


def mydialog(shp,*argus):
    for point in shp:
        myDialog = QtWidgets.QDialog()
        ui = Ui_Dialog()
        ui.setupUi(myDialog)  # setupUi()是由.ui文件生成的类的构造函数（初始化界面）
        myDialog.show()
        sys.exit(myDialog.exec_())  # 如果没有这个函数，则对话框闪退


if __name__ == '__main__':
    display, start_display, add_menu, add_function_to_menu = init_display()
    P0=gp_Pnt(0,0,1)
    P1 =gp_Pnt(0, 30, 20)
    menu_name = '打开'
    menu_name2 = '绘制模型'
    add_menu(menu_name)
    add_menu(menu_name2)
    display.DisplayShape(P0)
    display.SetSelectionModeVertex()  # 启动点的选中功能
    display.register_select_callback(mydialog)   #点击执行对话框
    start_display()
```
结果如图所示：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20181209194337318.?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80Mjc1NTM4NA==,size_16,color_FFFFFF,t_70)
