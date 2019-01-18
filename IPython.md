# 1. 安装  
## 1.1 pip安装  

1. **windows:**  
    ```
    curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py  
    python get-pip.py  
    ```  
3. **debian下：**  
+ **Python 2:**  
    ```
    sudo apt install python-pip  
    ```  
+ **Python 3:**  
    ```
    sudo apt install python3-pip  
    ```
  
## 1.2 IPython 安装 
    ```
    sudo pip3 install --upgrade pip  
    sudo pip3 install jupyter   
    ```
# 2. **运行IPython**  
+ **启动**
	>ipython
+ **退出**
	 >exit
	  
# 3. **IPython使用**  
+ **_的使用**
在 Python shell 下 _ 总是被赋予之前最后一个表达式的值
    ```  
    In [11]: s = "hello"

    In [12]: s
    Out[12]: 'hello'

    In [13]: a = _

    In [14]: a
    Out[14]: 'hello'
    ```
+ ****
    ```
    
    ```
+ ****
    ```
    
    ```
+ ****
    ```
    
    ```
+ ****
    ```
    
    ```
+ ****
    ```
    
    ```
+ ****
    ```
    
    ```
+ ****
    ```
    
    ```
+ ****
    ```
    
    ```
+ ****
    ```
    
    ```                        
+ **reset调试交互执行环境**  
reset  
  
+ **显示历史**  
history -n  
  
+ **重新执行history命令**  
%recall n-m  
  
+ **定义任何系统shell cmd别名**  
alias ipc ipconfig /all  
  
+ **save history 1-4行成外部文件**  
%save d:\1.py 1-4  
  
+ **save cell内容到外部文件**  
%save or write d:\1.py  
  
+ **编辑外部文件（windows）**  
%edit d:\1.py  
  
+ **执行外部文件**  
+ 调用外部python执行  
！python d:\1.py  
  
+ 内部空间执行  
+ %load d:\1.py or  
+ %prun d:\1.py or  
+ %run [-d] d:\1.py  
  


<!--stackedit_data:
eyJoaXN0b3J5IjpbMTE0OTQyMjAwM119
-->