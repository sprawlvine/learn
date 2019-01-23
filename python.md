
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

# 3. 知识点滴
## list

 - count <br> 
	```
     In [20]: a
    Out[20]: [2, 1, 4, 5, 6]
    
    In [24]: a.count(1)
    Out[24]: 1
	```
	
 - extend
	```   
    In [17]: a
    Out[17]: [2, 1]
    
    In [18]: a.extend?
    Docstring: L.extend(iterable) -- extend list by appending elements from the iterable
    Type:      builtin_function_or_method
    
    In [19]: a.extend([4,5,6])
    
    In [20]: a
    Out[20]: [2, 1, 4, 5, 6]
	```
  
# 4. 包管理
**安装**：
pip – Python 包和依赖关系管理工具。  

**仓库管理**：
 PyPI
warehouse – 下一代 PyPI。  

**打包**：
PyInstaller – 将 Python 程序转换成独立的执行文件（跨平台）。  
dh-virtualenv – 构建并将 virtualenv 虚拟环境作为一个 Debian 包来发布。  
Nuitka – 将脚本、模块、包编译成可执行文件或扩展模块。   
py2exe – 将 Python 脚本变为独立软件包（Windows）。  
pynsist – 一个用来创建 Windows 安装程序的工具，可以在安装程序中打包 Python本身。

**分发**：
wheel – Python 分发的新标准，意在取代 eggs。
  
  
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
+ **chardet** 
+  **re**
+  **fuzzywuzzy**
  模糊字符串匹配
  
+ **phonenumbers**   
+  
+  **PLY**
  lex 和 yacc 解析工具的 Python 实现

#### office 文件操作  
+ **openpyxl**
  读写 Excel 2010 xlsx/xlsm/xltx/xltm 文件
+ **XlsxWriter**  
+ **xlwt / xlrd**

+ **python-docx**  
  读取，查询以及修改 Microsoft Word 2007/2008 docx 文件

+ **CSV**  
  csvkit – 用于转换和操作 CSV 的工具。

+ **Jinja2** 
  一个现代的，对设计师友好的模板引擎。
  
### 命令行   
+ **click**  
+ 
+ **colorama** 
  跨平台彩色终端文本。

+ **bashplotlib** 
  在终端中进行基本绘图。
  
### 文件、目录处理
+ **shutil**     
  shutil - Utility functions for copying and archiving files and directory trees  
 
 +  **glob**  
  Use Unix shell rules to fine filenames matching a pattern.

+ **imghdr**  
  检测图片类型

+ **watchdog**
  管理文件系统事件的 API 和 shell 工具
 
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
  

### 爬虫
+ **Scrapy** 
  快速高级的屏幕爬取及网页采集框架。  

+ **cola** 
 一个分布式爬虫框架。  
 
+ **Demiurge** 
  基于PyQuery 的爬虫微型框架。
    
+ **MechanicalSoup** 
  自动和网络站点交互的 Python 库。 
    
+ **portia – Scrapy** 
可视化爬取。  

+ **pyspider** 
  一个强大的爬虫系统。 

+ **textract** 
  从任何格式的文档中提取文本，Word，PowerPoint，PDFs 等等。

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
+ **algorithms** 
  一个 Python 算法模块  
  
+ **python-patterns** 
  Python 设计模式的集合。

### json
+ **json/simplejson**  

### ssh
+ **paramiko**

### 缓存
+ **redis**

### 数据库
+ **mangodb**
+ **pymysql**
+ **cassandra-python-driver**  
 Cassandra 的 Python 驱动。  
 
 + **HappyBase**  
一个为 Apache HBase 设计的，对开发者友好的库。

### 图像处理
+ **PIL**  

+ **pyBarcode**  
  条形码
  
+ **python-qrcode**
  二维码生成器

+ **OCR**
pyocr – Tesseract 和 Cuneiform 的一个封装(wrapper)。  
pytesseract – Google Tesseract OCR 的另一个封装(wrapper)。
  
### 科学计算
+ **numpy**
+  **scipy**

### 数据处理
+ **pandas**

### 图形
+ **matlotlib**

### 机器学习
+ **scikit-learn**   
+  **xgboost**  
+  **nltk**  
+  **jieba**  
+   **gensim**

### 深度学习

 - **theano**
 - **keras**
 - **tensorflow**
 - **tflearn**
 - **tensorlayer**

### 其它
+ **functools**
 
+  **pprint**  

+  **Flake8**
    静态检查工具

+ **atexit**
 


<!--stackedit_data:
eyJoaXN0b3J5IjpbNzc1NzIzODcwLC0xNTg1NDE0NTY0LDc3MT
Y4Njg4MCwxNDMxMTkxNzU5LC04MDUwNTg0OTEsMTM3OTEwMTY4
OCwtOTQ5MTQ4MzQwLDIzOTAyNjY5NSwxMTU4NzEzODcwLDE2ND
MwMTM0ODIsODk5NzE4MjY2LDczMDk5ODExNl19
-->