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
 - **cmd 命令行运行**<br>
 这是一个字符界面<br>
	```
	D:\>ipython
	或
	D:\>ipython3
	```
 - **qtconsole运行**<br>
     这是一个图形界面<br>
	 ```
	 D:\>jupyter qtconsole
     ```
     
 - **退出**<br>
	`In [15]: exit`

  - **reset调试交互执行环境** <br> 
    ```	  
    In [194]: %reset
    Once deleted, variables cannot be recovered. Proceed (y/[n])?
    ```
- **%cls清屏**  <br>

## 3.2 **查询信息** 
 - **简单查询？**<br>
 显示用法<br>
 `object?`   -> Details about 'object'.

 - **详细查询？？**<br>
 显示详细的代码<br>
`object??`  -> More detailed, verbose information about 'object'.

 - **who，whos查看变量**<br>
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
 
## 3.3 **TAB提示自动补全**
 输入部分字符，按`TAB键`，自动提示
 
## 3.4 **调用shell 命令**
 - **!cmd**<br>
 在命令前面加上 `!` 则它会被作为命令行命令执行，这样你就不用`退出` IPython 来进行命令行操作<br>
    ```
    In [15]: !cd
    D:\work\learn
    
    In [16]: !ls
    docker.md             markdown    python             
    
    In [17]: !pwd
    /d/work/learn


    ```
## 3.5 **运行程序文件、测量、调试**   
 - **%run test.py**<br>
**手工调用调试**<br>
在当前环境下直接执行 `test.py`，效果跟命令行下调用 `python test.py` 相同, 相当于` %load + enter`, 如果启动debug调试，加`-d`，即`%run -d test.py`，然后就可以进入pdb进行详细的调试了

 - **程序中插入IPython断点调试**<br>
   如果程序是由命令行开始执行的，即在命令行下输入 `python test.py`（大部分 Python 程序都是），那么你还可以利用 IPython 在你的程序任意地方进行断点调试！<br>
    ```   
    import IPython as ipy
    
    ipy.embed()
   ```
 - **%time**<br>
`%time fun()` 跟 `timeit decorator` 作用类似，进行简单的 `一次`运行profile。<br>
      ```
    In [150]: %time a=1
    Wall time: 0 ns   
   ```   
   
  - **%timeit** <br>
 进行profile测量<br>
   ```
   In [149]: %timeit a=1
   19.1 ns ± 0.844 ns per loop (mean ± std. dev. of 7 runs, 10000000 loops
   each)
   ```
   
- **%prun**<br>
测试程序中每个函数消耗的时间<br>
    ```
       In [232]: %prun np.random.randn(3)
             4 function calls in 0.000 seconds
             ...
    ```

- **快速debug调试**<br>
-- **自动进入pdb**<br>
当%pdb自动模式打开时，一旦运行程序出错，自动进入pdb模式   <br> 
```
    In [249]: %pdb
    Automatic pdb calling has been turned ON 

      In [250]: a=d
    ---------------------------------------------------------------------------
    NameError                                 Traceback (most recent call last)
    <ipython-input-250-f3f3225a8e96> in <module>
    ----> 1 a=d
    
    NameError: name 'd' is not defined
    > <ipython-input-250-f3f3225a8e96>(1)<module>()
    ----> 1 a=d
    
    ipdb>
```

   -- **手动快读进入debug**<br>
```
    In [251]: %pdb
    Automatic pdb calling has been turned OFF
    
    In [252]: a=d
    ---------------------------------------------------------------------------
    NameError                                 Traceback (most recent call last)
    <ipython-input-252-f3f3225a8e96> in <module>
    ----> 1 a=d
    
    NameError: name 'd' is not defined
    
    In [253]: %debug
    > <ipython-input-252-f3f3225a8e96>(1)<module>()
    ----> 1 a=d
    
    ipdb>
```

## 3.6 **历史记录及外部文件操作**    
 - **%hist**<br>
 `%hist` 能显示之前输入过的命令的历史，`-n`显示行号。
 
 - **%save**<br>
保存指定行的历史记录到文件，如保存130-131行到test.py<br>
     ```
    In [139]: %save test.py 130-131
    The following commands were written to file `test.py`:
    a = range(12)
    for i in a: print(i)
   ```

 - **%pycat**<br>
 查看python代码文件<br>
    ``` 
    In [228]: %pycat test.py
    # coding: utf-8
    a = range(12)
    for i in a: print(i)
   ``` 
 - **%edit** <br>
     打开编辑器，关闭编辑器，代码会自动执行：）<br>
     ```
     In [147]: %edit test.py
     Editing... done. Executing edited code...
   ```
  
- **%writefile**<br>
编辑并写入外部文件<br>
    ```
        In [238]: %%writefile test2.py
         ...: a = 1
         ...: b = 1
         ...: a
         ...:
         ...:
         ...: 
    ```      
 - **%load**<br>
load文件并执行<br>
`In [140]: %load test.py`
    
     
 - **重新执行history命令**  <br>
%recall n-m  <br>
    ```
     In [172]: %recall 150

     In [173]: %time a=1
     Wall time: 0 ns
   ```  

 ## 3.7 **其它操作**    

 - **lsmagic命令**<br>
显示所有的magic命令

- **%env**<br>
可以查看以及设置环境变量<br>
In [173]: %env

 - **定义任何系统shell cmd别名**<br>  
`In [173]: alias ipc ipconfig /all ` 

 - **%automagic**<br>
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
eyJoaXN0b3J5IjpbNjE5OTU0NTcwXX0=
-->