# Windows高效率工作工具集合简介

## 1. 包安装/卸载工具

- **chocolatey**

  windows的apt-get，安装gui `choco install chocolateygui`，后图形界面很直观，里面的软件很多，程序员用的基本都有了，一站式购物，很方便，免得到处去下载，无缘无故中各种流氓全家桶，很实用，有一点美中不足，就是没有中文的软件，不过不是什么大问题，需求量比较小，国内公司的软件到官方网站下载即可

- **GeekUninstaller**  
  chocolatey中有，一键安装，彻底卸载工具，小而精致

## 2. 文件管理

- **Total Commander**  
  chocolatey中有，一键安装，多窗口多tab文件管理器，完爆window文件管理器，并且`CTRL+Q`快速预览选定文件

  **提示：**  
  TC默认右键为选定，一般很不习惯，可以通过 `配置->操作->通过左键选择` ，这样右键菜单就回来了

## 3. 文件快速定位、搜索

- **listary**  
  chocolatey中有，一键安装，快速文件搜索定位工具，安装完成后，`CTRL+CTRL`，神速定位

- **everything**  
  chocolatey中有，一键安装，很全面的文件搜索工具，可以做成web的搜索，可以作为listary的补充

## 4. 快速启动

- **wox**
  chocolatey中有，一键安装，快速启动程序，安装完成后，`ALT+SPACE`，快速启动，不用点半天菜单，找程序了

## 5. 剪切板工具

- **ditto**
  chocolatey中有，一键安装，剪切板工具，windows自带的剪切板是在是弱爆了，安装完成, **CTRL+\`** 一键呼出剪切板历史

## 6. 文本编辑

- **Notepad++**  
  chocolatey中有，一键安装，纯文本编辑器，比Ultraedit要快，免费

## 7. 文件预览

- **quicklook**
  chocolatey中有，一键安装，快速预览工具，支持大部分的文档格式，安装完成后，选定文档，`空格`预览

## 8. 截图、录像工具

- **snipaste**  
  chocolatey中有，一键安装，截屏神器，安装完成后`F1`截屏

- **ScreenToGif**  
  chocolatey中有，一键安装，屏幕录像转Gif神器

## 9. cmd工具

- **cmder**
多窗口tab管理，一键打开**cmd、powershell、bash、minitty**窗口，集成**git、vim**
  - **打开、关闭窗口**

    CTRL + T / CTRL + W

  - **鼠标右键集成**

    `Cmder.exe /REGISTER ALL`

  - **解决中文乱码**

    在设置中修改Environment

    `set LANG=zh_CN.UTF-8`

  - **git status时中文文件名乱码**

    ```text

    现象：

    \344\275\240\345\245\275
    执行以下命令即可：

    git config --global core.quotepath false
    ```

## 10. 远程连接及终端

- **MobaXterm**

  **远程连接的神器，能同时图形化显示远程目录和termial，比putty好得多**

- **WinSCP**

  SCP/SFTP工具，很好用

- **VNC Viewer**

  很好用的linux远程桌面工具，windows上Team view用的更多一些

- **putty**

  远程连接用的很多的工具，界面丑陋点，没有其它工具可用的情况下，稳定能用

## 11. 系统空间查看工具

- **SpaceSniffer**

  图形化平铺显示系统的disk占用，直观得让你不敢相信

- **WizTree**

  文件磁盘占用扫描，速度快得不可想象

## 12. 系统清理

- **CCleaner**

  良心系统清理工具，Free版已经很好用了，你可以把3x0扔了

## 13. 编程工具集

- **Visual Studio Code**

  通用编程IDE，丰富的插件，通过配置可以配置C/C++，Python，Markdown等各种编程环境，
  [入门参考：](https://github.com/sprawlvine/learn/blob/master/IDE/vscode.md)