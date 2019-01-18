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
 - **运行**
	```
	D:\>ipython
	或
	D:\>ipython3
	```
 - **退出**
	`In [15]: exit`

  - **reset调试交互执行环境**  
    ```	  
    In [194]: %reset
    Once deleted, variables cannot be recovered. Proceed (y/[n])?
    ```
	
## 3.1 **查询信息** 
 - **简单查询？**
 `object?`   -> Details about 'object'.
 - **详细查询？？**
`object??`  -> More detailed, verbose information about 'object'.
 
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
在当前环境下直接执行 `test.py`，效果跟命令行下调用 `python test.py` 相同, 相当于
    > %load + enter。

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

 - **定义任何系统shell cmd别名**  
`In [173]: alias ipc ipconfig /all ` 

 - **%automagic**
`%automagic` 是打开的状态的话，所有 magic function 不需要在前面加 `%` 就能正确调用。
           

  

  

  
 


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEyOTU3MDg3MzJdfQ==
-->