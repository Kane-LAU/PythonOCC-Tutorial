上一篇：[**创建pythonocc虚拟环境**](https://blog.csdn.net/weixin_42755384/article/details/84138407)
使用pythonocc作为开发库，那么我们也应该有一个python IDE，我选择的是pycharm，下面的例子也会使用pycharm来示范，当然其他的IDE也是可以的，比如spyder等
### 一、利用pycharm建立一个pythonocc项目
打开pycharm
File->New Project 建立一个新项目
![在这里插入图片描述](https://img-blog.csdnimg.cn/20181209155051910.?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80Mjc1NTM4NA==,size_16,color_FFFFFF,t_70)
然后配置外部环境，配置好后create
![在这里插入图片描述](https://img-blog.csdnimg.cn/20181209155623324.?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80Mjc1NTM4NA==,size_16,color_FFFFFF,t_70)

### 二、写第一个程序
在pycharm中创建好的项目上，右键选择
![在这里插入图片描述](https://img-blog.csdnimg.cn/20181209160021725.?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80Mjc1NTM4NA==,size_16,color_FFFFFF,t_70)
随便取个名字
![在这里插入图片描述](https://img-blog.csdnimg.cn/20181209160149792.)
接下来，我们会编写一个程序：
**你也可以直接在这里下载文档：[pythonocc第一个小程序]**(https://download.csdn.net/download/weixin_42755384/10838556)
```
#第一个程序，在显示框中显示两个点
from OCC.Display.SimpleGui import init_display
from OCC.gp import gp_Pnt
if __name__ == '__main__':
    display, start_display, add_menu, add_function_to_menu = init_display()
    P0=gp_Pnt(0,0,1)
    P1 =gp_Pnt(0, 30, 20)
    display.DisplayShape(P0)
    display.DisplayShape(P1)
    start_display()
```
在test.py上右键，run“test.py”
![在这里插入图片描述](https://img-blog.csdnimg.cn/201812091613052.?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80Mjc1NTM4NA==,size_16,color_FFFFFF,t_70)
最终结果如图所示：![在这里插入图片描述](https://img-blog.csdnimg.cn/20181209161448659.?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80Mjc1NTM4NA==,size_16,color_FFFFFF,t_70)
***下一篇***：[**创建属于自己的主界面及对话框及安装qtdesigner**](https://blog.csdn.net/weixin_42755384/article/details/84403098)
***如果你遇到了问题，请在这里寻找答案***：[**pythonocc常见问题集锦**](https://blog.csdn.net/weixin_42755384/article/details/84187626)
