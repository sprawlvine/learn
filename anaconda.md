
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
# 3. 创建新的virtual env
## 3.1 图形界面
    Anaconda Navigator图形界面 --> Envrioments --> create
## 3.2 cli界面
