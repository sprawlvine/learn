
# 1. Install
## 1.1 windows
- 点击下载：[anaconda for windows](https://www.anaconda.com/distribution/#windows)
## 1.2 linux
- 点击下载：[anaconda for linux](https://www.anaconda.com/download/#linux)
- 安装:
  + **python 3.x**
  ```
  bash ~/Downloads/Anaconda3-5.3.0-Linux-x86_64.sh
  ```
  + **python 2.x**
  ```
  bash ~/Downloads/Anaconda2-5.3.0-Linux-x86_64.sh
  ```
## 1.3 安装确认
打开 Anaconda Navigator(linux在terminal下敲: anaconda-navigator)，能打开，则确实安装成功

# 2. Update
## 2.1 **升级anaconda**：
```
conda update conda
conda update anaconda
```
## 2.2 **升级navigator**
```
conda deactivate
conda update anaconda-navigator
```
# 3.virtuale env的创建和切换使用
## 3.1 创建新的virtual env
### 3.1.1 图形界面
    Anaconda Navigator图形界面 --> Envrioments --> create
### 3.1.2 cli界面
    Anaconda prompt->
    conda create --name py2.7 python=2.7
## 3.2 使用和包管理
### 3.2.1 图形界面
- **查看、切换env**
  > 段落引用Anaconda Navigator图形界面 --> Envrioments --> 点击选中相应的env，切换
- **包的管理**
  > 可以通过搜索框输入，并通过filter框过滤查看，然后点击相应的包进行install、update，uninstall
### 3.2.2 anaconda cli界面
- **查看env list**
    > conda info -e
- **切换env**
    > active py2.7
- **包安装管理**
    > pip 自行安装管理
