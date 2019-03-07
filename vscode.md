
# 1. 安装

window安装比较简单去官方下载即可，linux安装参考如下：
[官方参考](https://code.visualstudio.com/docs/setup/linux)
following script:

- The repository and key can also be installed manually with the

```curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > microsoft.gpg
sudo install -o root -g root -m 644 microsoft.gpg /etc/apt/trusted.gpg.d/
sudo sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main" > /etc/apt/sources.list.d/vscode.list'
```

- Then update the package cache and install the package using:

```sudo apt-get install apt-transport-https
    sudo apt-get update
    sudo apt-get install code # or code-insiders
```

# 2. 配置

## 2.1 python开发

python工程开发，如果文件较大，逻辑较复杂，vscode的outline可能解析得不是很顺畅，可以考虑用pycharm配合anaconda开发，中小工程快速开发用vscode很顺手？真的吗？安装完下面插件之后，我有点怀疑是不是可以继续这么吹pycharm ：）

有一些必备的插件，安装之后vscode好用得能起飞：

- **python**
  >微软官方插件，python支持必备
- **Anaconda Extension Pack**
  > Anaconda的vscode支持包，很好支持第三方包的补全
- **neuron**
  >集成了jypyter notebook的代码片段交互调试，需要先安装jupyter notebook
- **Visual Studio IntelliCode**
  >微软AI辅助编程
- **One Dark Pro**
  >让代码五颜六色，大大提高可读性
- **Bracket Pair Colorizer**
  >括弧加了颜色，多个嵌套括弧一目了然
- **vscode-icons**
  >文件的图标生动化
- **Material Icon Theme**
  >配合上面使用，更多的icon主题
- **Path Autocomplete**
  >在代码里书写文件路径的时候自动补全，非常方便
- **Better Comments**
  >通过！？Todo*支持警告，疑问，todo，高亮注释，更加可读
- **autoDocstring**
  >注释自动补全，并且格式很清晰
- **Python Preview**
  >可以预览代码执行，并且数据结构是图形化的直观展示
- **Todo Tree**
  >自动抽取代码中的todo，高亮，并且可以以树的形式展现出来，方便编码
- **Trailing Spaces**
  >高亮行位的空格，并且可以一键删掉
- **TabOut**
  >对于能够自动补全“（的编辑器来说，自动补全之后，需要向后移动光标，非常不方便，这个插件可以用tab键自动跳出去，很高效
- **GitLens**
  >真的是git放大镜，很方便查看日志，比较
- **Git History**
  >图形化显示日志

## 2.2 markdown

- **Markdown All in One**
  >markdown支持
- **Markdown Preview Github Style**
  >把默认的slide preview替换成github风格的
- **Markdown Preview Enhanced**
  >功能比较全的预览支持
- **Markdown Shortcuts**
  >输入快捷键，右键或者CTRL+SHIFT+P可以输入很多markdown语法，提高输入效率，有了它，没有toolbar也无妨
- **markdownlint**
  >语法检查器，这个挺好，能让markdown文档写得很规范
- **Markdown Preview Meraid support**
  >流程图支持
- **Mermaid Preview**
  >流程图预览支持

## 2.3 思维导图

- **mindmap**
  >简单的思维导图，写文档的时候可以画一些思路，然后存成图片，导入github等图床

## 2.4 配置

- **Settings Sync**
  >github上利用gist存储vscode的配置，存上去，随时取下来，不用反复配置了

# 3. 基本使用

- **workspace**
  > workspace包含了一组目录和文件，类似工程的概念
- **显示符号表**
  > 点击 `explore`窗口，`outline`
- **多行注释快捷键**
  > ctrl + shit + A
- **单行注释快捷键**
  > ctrl + /

# 4. debug

## 4.1 python

Debug菜单——>左下角选择好python的编译器,然后可以进行local或者remote的debug，
remote debug需要ptvsd的支持。

`Enjoy it！`