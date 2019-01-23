
# 1. 开发环境
+ **ipython**
[ipython入门](https://github.com/sprawlvine/learn/blob/master/IPython.md)

# 2. python环境管理
p
pyenv
vex
virtualenvwrapper

+ **virtualenv**  
  创建独立 Python 环境的工具
  
# 3. 包管理
pip – Python 包和依赖关系管理工具。  
pip-tools – 保证 Python 包依赖关系更新的一组工具。  
conda – 跨平台，Python 二进制包管理工具。  
Curdling – 管理 Python 包的命令行工具。  
wheel – Python 分发的新标准，意在取代 eggs。

**本地 PyPI 仓库服务和代理**

warehouse – 下一代 PyPI。  
Warehousebandersnatch – PyPA 提供的 PyPI 镜像工具。  
devpi – PyPI 服务和打包/测试/分发工具。  
localshop – 本地 PyPI 服务（自定义包并且自动对 PyPI 镜像）。


**分发**

打包为可执行文件以便分发。

PyInstaller – 将 Python 程序转换成独立的执行文件（跨平台）。  
dh-virtualenv – 构建并将 virtualenv 虚拟环境作为一个 Debian 包来发布。  
Nuitka – 将脚本、模块、包编译成可执行文件或扩展模块。  
py2app – 将 Python 脚本变为独立软件包（Mac OS X）。  
py2exe – 将 Python 脚本变为独立软件包（Windows）。  
pynsist – 一个用来创建 Windows 安装程序的工具，可以在安装程序中打包 Python本身。

  
  
作者：史豹  
链接：https://www.zhihu.com/question/20501628/answer/223340838  
来源：知乎  
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。
# 4. 常用库
## 4.1 参考
  **[vinta/awesome-python · GitHub](https://github.com/vinta/awesome-python)**

##  4.2 库说明

### 调试、度量、日志
+  **pdb**
+ **ipdb**
+  **traceback**
+  **logging**
+  **cprofile**
+  **timeit**
+ **dis**  
  反汇编

### 文本处理
+  **re**

### 命令行   
+ **click**  

### 文件目录处理
+ **shutil**     
  shutil - Utility functions for copying and archiving files and directory trees  
 
 +  **glob**  
  Use Unix shell rules to fine filenames matching a pattern.

### 事件调度处理   
+ **sched**  
  The [sched](https://pymotw.com/2/sched/index.html#module-sched "sched: Generic event scheduler.") module implements a generic event scheduler for running tasks at specific times  

### 上下文  
+ **contextlib**    
  contextlib - Utilities for with-statement contexts  

### 线程、进程  
+ **multiprocessing**   
  This package is intended to duplicate the functionality (and much of
  the API) of threading.py but uses processes instead of threads.  A
  subpackage 'multiprocessing.dummy' has the same API but is a simple
   wrapper for 'threading'.  

+  **threading** 


### 系统、shell交互
+ **os**
+ **subprocess**  
+ **sh**
  sh is a full-fledged subprocess replacement
  
### web
+ **flask**  

+ **django**

+  **SimpleHTTPServer** 
 
+ **urllib/urllib2/httplib**  
  偏底层
  
+  **requests**
  人性化的HTTP请求库

+ **lxml**

+  **httpie**  
  一个命令行HTTP 客户端，cURL 的替代品，易用性更好

+  **you-get**  
  一个 YouTube/Youku/Niconico 视频下载器  
  
+  **youtube-dl**
  用来下载 YouTube 视频的工具

+ **pycurl**
     cURL library module for Python

+ **xmltodict**   
  xml转dict
  
+ **scrapy** 

### 迭代器    
+  **itertools**
  迭代器

### 序列化、反序列化
+  **pickle/cPickle**
  The [`pickle`](https://docs.python.org/3/library/pickle.html#module-pickle "pickle: Convert Python objects to streams of bytes and back.") module implements binary protocols for serializing and de-serializing a Python object structure

### 数据结构
+  **collections** 
+  **queue**
 A thread-safe FIFO implementation

### 算法
+ **hashlib md5, sha**   

### json
+ **json/simplejson**  

### ssh
+ **paramiko**

### 缓存
+ **redis**

### 数据库
+ **mangodb**

### 图像处理
+ **PIL**  

### 科学计算
+ **numpy**
+  **scipy**

### 图形
+ **matlotlib**
+ 
### 其它
+ **functools**
 
 
+  **pprint**  

+  **Flake8**
    静态检查工具

+ **atexit**
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTcxNTU0MDA0LDExNTg3MTM4NzAsMTY0Mz
AxMzQ4Miw4OTk3MTgyNjYsNzMwOTk4MTE2XX0=
-->