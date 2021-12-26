
使用目的：做个小工具，只有简单的两三个功能，使用命令行不是非常方便，因此尝试用GUI做。

存在以下条件：

1.  只需要在Win上使用，不需要考虑跨平台
2.  支持win32api
3.  支持打包成exe文件，且体积足够小

从自己的技能树来看，比较适合的选择有：

+ PySide/PyQt
+ WxPython
+ Electron

最终选择了PySide6来使用。Electron存在打包体积过大的情况（打包完大概有60多M，PySide6大概是30多M，WxPython则是20M左右）。PySide和WxPython对比差距不太大，考虑了一下还是先学了PySide6，了解一下QT框架。

选择了Python，则涉及到两个打包工具，分别是

+ pyinstaller
+ Nuitka

pyinstaller 老牌打包工具了，但是存在打包体积大，编译慢等问题。Nuitka 的话则在速率和打包体积上都有更好的效果，但目前来看bug还比较多。我这边win32event 编译完后还是无法使用，显示import error。Nuitka的使用可见[[使用Nuitka打包pyside6编写的GUI]]

做GUI遇到最大的问题就是不懂怎么做好布局？这个在之前学前端的时候也遇到过，不过通过各种强大的UI库规避掉了。但在搞QT需要自己设置的时候就暴露的很明显

目前的小工具还是用QTWidget做的，后续可以看下QML~



