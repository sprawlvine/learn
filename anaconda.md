
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
# 3.virtuale env的管理和切换使用
## 3.1 创建新的virtual env
### 3.1.1 图形界面
    Anaconda Navigator图形界面 --> Envrioments --> create
### 3.1.2 cli界面
    Anaconda prompt->
    conda create --name py2.7 python=2.7
## 3.2 使用env和env的包管理
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
**conda自动解决依赖关系**，++推荐用conda安装++，但是一些第三方包，conda会找不到，用pip安装即可
    > pip 安装管理 
    或者
    > conda install [-c conda-forge] scrapy
      其中-c是选择channel，即包的源
  - **安装好后，查看当前环境中已经安装的包**：
    conda list
  - **添加 --name 参数安装包到指定环境**
    conda install --name 环境名 click
  - **升级指定依赖包**
    conda update click
    
## 3.3 env的export和import
### 3.3.1 图形界面
    在Navigator的Enviroments中clone，import
### 3.3.2 CLI界面
```
conda env export > testenv.yaml
conda env create --name testclone -f testenv.yaml
```

## 3.3 env的删除
### 3.3.1 图形界面
    在Navigator的Enviroments中remove
### 3.3.2 CLI界面
```
conda env remove --name testclone
```

## 3.4 在vscode
OS的Terminal如何切换env