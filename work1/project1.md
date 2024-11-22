#  UE5.4安装与打包个人学习手册

## UE引擎源码编译

首先通过官网下载相关的源码，按照他md手册中进行，

首先运行setup.bat运行，因为相对较大，我们可以选择采用多线程的方式进行下载，然后生成解决方案

**注意点（其实就是个人踩过的坑）：**记得将**UE5设置为启动项目**进行编译，同时根据手册，记得将编译工具设置为MSCV14.38，通常默认的都是最新，但是会出现问题，存在未定义的宏，此外编译工具解决方案配置一定要是Development Editor,不然最后会显示一个缺少文件

<img src=".\images\屏幕截图 2024-11-22 162947.png" alt="屏幕截图 2024-11-22 162947" style="zoom: 50%;" />

编译完成之后，UnrealEngine-5.4.4-release\Engine\Binaries\Win64下，大小估计180，不过中间过程超过300g还是预留些。

最后打开UE

<img src=".\images\屏幕截图 2024-11-22 163402.png" style="zoom:50%;" />

创建完项目之后会需要打开项目文件的解决方案然后再次编译。

会得到之后的界面

<img src=".\images\屏幕截图 2024-11-22 163838.png" style="zoom: 33%;" />

然后打包流程可能相对就比较麻烦，然后这边我是找了https://youtu.be/JdK-zIeIPY0?si=wbzXqtryQNNJNyHI这样一个视频结合官方手册，然后基本上就能配置成功，

在这个过程中我主要遇到的一个麻烦就是向手机索要存储权限，看了下UE社区大致说法就是sdk33之后好像都会存在这样的问题，只要切换到32就可以，也是上面的视频所采用。但看了下其中还有种办法就是https://ue5hub.com/forum-post/1930.html这里面采用的直接build时提供。另一种就是我所采用的简单粗暴的直接关掉加载界面。

最后打包出来的就是我给出的那个，然后成功的运行出来。

<img src="file:///C:\Users\lenovo\Documents\Tencent Files\2461785659\nt_qq\nt_data\Pic\2024-11\Ori\34030d3caa27282327fea8ed540b46b9.jpg" alt="img" style="zoom:25%;" />