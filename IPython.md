# 1. 安装  
## 1.1 pip安装  

1. **windows:**  
    ```
    curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py  
    python get-pip.py  
    ```  
3. **debian下：**  
+ **只有一份python环境或者多份环境下的Python 2:**  
    ```
    sudo apt install python-pip  
    ```  
+ **Python 3:**  
    ```
    sudo apt install python3-pip  
    ```
  
## 1.2 IPython 安装 
    ```
    只有一份python环境或者多份环境下的python2:
    sudo pip install ipython
    sudo pip install jupyter
    
    python3:
    sudo pip3 install ipython  
    sudo pip3 install jupyter 
    
    或者
    
    只有一份python环境或者多份环境下的python2:
    sudo python -m pip install ipython  
    sudo python -m pip install jupyter
    
    python3:
    sudo python3 -m pip3 install ipython  
    sudo python3 -m pip3 install jupyter
    ```
问题：
如果出现  `ImportError: cannot import name 'create_prompt_application'`  
downgraded the prompt-toolkit to the version 1.0.15 and jupyter worked again.
或者 卸载 ipython重新安装

 
# 3. **IPython使用**  
## 3.1. **运行/退出**  
 - **cmd 命令行运行**
 这是一个字符界面
	```
	D:\>ipython
	或
	D:\>ipython3
	```
 - **qtconsole运行**
     这是一个图形界面
	 ```
	 D:\>jupyter qtconsole
     ```
     
 - **退出**
	`In [15]: exit`

  - **reset调试交互执行环境**  
    ```	  
    In [194]: %reset
    Once deleted, variables cannot be recovered. Proceed (y/[n])?
    ```
- **%cls清屏**  

## 3.1 **查询信息** 
 - **简单查询？**
 显示用法
 `object?`   -> Details about 'object'.

 - **详细查询？？**
 显示详细的代码
`object??`  -> More detailed, verbose information about 'object'.

 - **who，whos查看变量**
    ```
    In [219]: who
    IPython  a       b       c       i       ip      s       s1      s2
    s3       string  v

    In [220]: whos
    Variable   Type      Data/Info
    ------------------------------
    IPython    module    <module 'IPython' from 'd<...>s\\IPython\\__init__.py'>
    a          range     range(0, 12)
    b          str       hello
    c          str       hello
    i          int       11 
    ip         module    <module 'IPython' from 'd<...>s\\IPython\\__init__.py'>
    s          int       456
    s1         str       1
    s2         str       2
    s3         str       3
    string     module    <module 'string' from 'd:<...>ython36\\lib\\string.py'>
   ```
 
## 3.2 **TAB提示自动补全**
 输入部分字符，按`TAB键`，自动提示
 
## 3.3 **调用shell 命令**
 - **!cmd**
 在命令前面加上 `!` 则它会被作为命令行命令执行，这样你就不用`退出` IPython 来进行命令行操作
    ```
    In [15]: !cd
    D:\work\learn
    
    In [16]: !ls
    docker.md             markdown    python             
    
    In [17]: !pwd
    /d/work/learn


    ```
## 3.4 **运行程序文件、测量、调试**   
 - **%run test.py**
在当前环境下直接执行 `test.py`，效果跟命令行下调用 `python test.py` 相同, 相当于` %load + enter`, 如果启动debug调试，加`-d`，即`%run -d test.py`，然后就可以进入pdb进行详细的调试了

 - **%time**
`%time fun()` 跟 `timeit decorator` 作用类似，进行简单的 `一次`运行profile。
      ```
    In [150]: %time a=1
    Wall time: 0 ns   
   ```
   
 - **%timeit** 
 进行profile测量
   ```
   In [149]: %timeit a=1
   19.1 ns ± 0.844 ns per loop (mean ± std. dev. of 7 runs, 10000000 loops
   each)
   ```
   
 - **程序中插入IPython断点调试**
   如果程序是由命令行开始执行的，即在命令行下输入 `python test.py`（大部分 Python 程序都是），那么你还可以利用 IPython 在你的程序任意地方进行断点调试！
```   
    import IPython as ipy
    
    ipy.embed()
```
## 3.5 **历史记录操作**    
 - **%hist**
 `%hist` 能显示之前输入过的命令的历史，`-n`显示行号。
 
 - **%save**
保存指定行的历史记录到文件，如保存130-131行到test.py
     ```
    In [139]: %save test.py 130-131
    The following commands were written to file `test.py`:
    a = range(12)
    for i in a: print(i)
   ```

 - **%edit** 
     打开编辑器，关闭编辑器，代码会自动执行：）
     ```
     In [147]: %edit test.py
     Editing... done. Executing edited code...
   ```
   
 - **%load**
load文件并执行
`In [140]: %load test.py`
     
 - **重新执行history命令**  
%recall n-m  
    ```
     In [172]: %recall 150

     In [173]: %time a=1
     Wall time: 0 ns
   ```  

 ## 3.6 **其它操作**    

 - **lsmagic命令**
显示所有的magic命令

 - **定义任何系统shell cmd别名**  
`In [173]: alias ipc ipconfig /all ` 

 - **%automagic**
`%automagic` 是打开的状态的话，所有 magic function 不需要在前面加 `%` 就能正确调用。
           
# 4. **jupyter使用**  
  
## 4.1. **运行/退出**  
 - **jupyter运行**
	```
	D:\>jupyter
	```
 - **qtconsole运行**
     这是一个图形界面console
	 ```
	 D:\>jupyter qtconsole
     ```
     
 - **退出**
	`In [15]: exit`
	
## 4.2. **notebook操作**
 - **创建一个Notebook** <br>
jupyter的菜单 <br>
File-->New Notebook-->Python3

 - **创建一个记录点**  <br>
notebook的菜单 <br>
File-->Save and Checkpoint

 - **返回到某一个记录点**  <br>
notebook的菜单 <br>
File-->Revert to Checkpoint

 - **下载notebook**  <br>
notebook的菜单 <br>
File--> Download as  
     ```
    ipynb
    py  
    md  
    html
    pdf
   ```

 - **关闭notebook** <br> 
notebook的菜单 <br>
 File--> Close and Halt

## 4.2. **cell编辑操作**
 notebook的菜单  <br>
 Edit-->
 Insert-->
包括复制、粘贴、删除、合并、移动

## 4.3. **cell运行**  
 notebook的菜单  <br>
 cell-->
 或者用图标工具栏

 - **cell内命令参考上面IPython console的命令**
 
 - **每个cell可以随时编辑重新运行，非常方便**

## 4.4. **有用的帮助**  
-   Python
-   IPython
-   NumPy
-   SciPy
-   MatPlotlib
-   SymPy
-   pandas

  
 


<!--stackedit_data:
eyJoaXN0b3J5IjpbMTg3NzQxMDQxM119
-->