
# 1. Install 
 - The repository and key can also be installed manually with the following script:
	```
    curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > microsoft.gpg
    sudo install -o root -g root -m 644 microsoft.gpg /etc/apt/trusted.gpg.d/
    sudo sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main" > /etc/apt/sources.list
    ```
.d/vscode.list'

 - Then update the package cache and install the package using:
	```
    sudo apt-get install apt-transport-https
    sudo apt-get update
    sudo apt-get install code # or code-insiders
    ```
# 2. 配置

## 2.1 python开发

    安装editorconfig插件
    
# 3. 使用  
- **workspace**
	```
    workspace包含了一组目录和文件，类似工程的概念
	```	
- **显示符号表**
	点击 `explore`窗口，`outline`
	
- **多行注释快捷键**
    > ctrl + shit + A	 
- **单行注释快捷键**
    > ctrl + /

