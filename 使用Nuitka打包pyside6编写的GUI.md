1. 安装nuitka


```
pip install nuitka
```

2. 安装mingw64

使用 nuitka 打包的时候按yes按提示安装即可，不需要单独安装

3. 打包命令行

```
.\pyside\Scripts\nuitka.bat --standalone --plugin-enable=pyside6 --windows-disable-console --show-progress --nofollow-imports --onefile .\hello.py
```

如果要在没有Python环境上执行exe，则需要加上`--onefile`参数
