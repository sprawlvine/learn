
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


<!--stackedit_data:
eyJoaXN0b3J5IjpbMjY3MDU4MDAzLDYxMjM0MzUzMSwtNTk4OD
c1MDMyLDczMDk5ODExNl19
-->