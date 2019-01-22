
# 1. Install 

 - The repository and key can also be installed manually with the following script:

    ```
curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > microsoft.gpg
sudo install -o root -g root -m 644 microsoft.gpg /etc/apt/trusted.gpg.d/
sudo sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main" > /etc/apt/sources.list.d/vscode.list'
   ```

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE5MDE4NjI4NTksNjEyMzQzNTMxLC01OT
g4NzUwMzIsNzMwOTk4MTE2XX0=
-->