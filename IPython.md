# 1. 安装  
## 1.1 pip安装  

1. **windows:**  
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py  
python get-pip.py  
  
2. **debian下：**  
+ **Python 2:**  
sudo apt install python-pip  
  
+ **Python 3:**  
sudo apt install python3-venv python3-pip  
  
## 1.2 IPython  
1. **PiP安装**  
pip3 install --upgrade pip  
pip3 install jupyter  
  
2. **Pandas**  
pip3 install pandas  
  
3. **IPython使用**  
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
  
# 2. Pands  
1.dataframe增加一行  
  
ds = pd.date_range("20180101", periods=7)  
df = pd.DataFrame(np.random.randn(7,4),index=ds,columns=list('abcd'))  
  
s2 = pd.Series([5,5,5,5])  
s2.index = df.columns  
df.append(s2)  
df.append(s2, ignore_index=True)  

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEwNTk2NjU0OV19
-->