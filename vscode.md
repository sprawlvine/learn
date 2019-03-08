<h1>目录</h1>
<!-- TOC -->

- [1. 安装](#1-%E5%AE%89%E8%A3%85)
- [2. 配置](#2-%E9%85%8D%E7%BD%AE)
  - [2.1. python开发](#21-python%E5%BC%80%E5%8F%91)
  - [2.2. Markdown](#22-markdown)
  - [2.3. 思维导图](#23-%E6%80%9D%E7%BB%B4%E5%AF%BC%E5%9B%BE)
  - [2.4. 配置](#24-%E9%85%8D%E7%BD%AE)
- [3. 基本使用](#3-%E5%9F%BA%E6%9C%AC%E4%BD%BF%E7%94%A8)
- [4. debug](#4-debug)
  - [4.1. python](#41-python)

<!-- /TOC -->

***

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

## 2.1. python开发

python工程开发，如果文件较大，逻辑较复杂，vscode的outline可能解析得不是很顺畅，可以考虑用pycharm配合anaconda开发，中小工程快速开发用vscode很顺手？真的吗？安装完下面插件之后，我有点怀疑是不是可以继续这么吹pycharm ：）

必备的插件，安装之后vscode好用得能起飞，插件安装好以后，有的插件直接在右键菜单出现，有命令的有的需要用F1或者CTRL+SHIT+P调出command palette，然后敲入插件名字，选择相应的命令：

- **核心插件**
  - **python**
    >微软官方插件，python支持必备
    >
    >**使用方式：启动自动调用**
  - **Anaconda Extension Pack**
    > Anaconda的vscode支持包，很好支持第三方包的补全
    >
    >**使用方式：启动自动调用**
- **调试运行**
  - **CodeRunner**
    >片断代码的调试利器，可以在左边代码窗口快速高效写代码，然后在右边的interactive窗口调试，单一交互窗口没有Ipython强大，结合编辑器用，比单用Ipython厉害多了
    >
    >**使用方式：右键或者F1，然后输入code runner选择命令**

  - **neuron**
    >集成了jypyter notebook的代码片段交互调试，可以通过右边的pannel窗口显示结果，然后再把pannel串口的cell在浏览器打开，以强大的notebook环境进行交互调试，演示等
    >
    >**使用方式：右键和右上角的图标**
  - **Python Preview**
    >可以预览代码执行，back/forward执行，除了正常的输出结果外，特点是会把其中的变量以图形化的方式直观展示,调试代码片断的时候非常强大
    >
    >**使用方式：F1，然后输入python preview选择命令**
- **代码编写**
  - **Visual Studio IntelliCode**
    >微软AI辅助编程
    >
    >**使用方式：启动自动调用**
  - **One Dark Pro**
    >让代码五颜六色，大大提高可读性
    >
    >**使用方式：启动自动调用**
  - **Bracket Pair Colorizer**
    >括弧加了颜色，多个嵌套括弧根据颜色一目了然
    >
    >**使用方式：启动自动调用**
  - **Path Autocomplete**
    >在代码里书写文件路径的时候自动补全，非常方便
    >
    >**使用方式：启动自动调用**
  - **Trailing Spaces**
    >高亮行位的空格，并且可以一键删掉
    >
    >**使用方式：F1，然后输入python trailing选择命令**
  - **TabOut**
    >对于能够自动补全“（的编辑器来说，自动补全之后，需要向后移动光标，非常不方便，这个插件可以用tab键自动跳出去，很高效
    >
    >**使用方式：启动自动调用**
- **文档化**
  - **autoDocstring**
    >注释自动补全，并且格式很清晰
    >
    >**使用方式：启动自动调用**
  - **Better Comments**
    >通过！？Todo*支持警告，疑问，todo，高亮注释，更加可读
    >
    >**使用方式：启动自动调用，编写注释时，自行输入!?todo\***
  - **Todo Tree**
    >自动抽取代码中的todo，高亮，并且可以以树的形式展现出来，方便编码
    >
    >**使用方式：启动自动调用,左边栏会出现todo图标**
- **IED Workspace环境优化**
  - **vscode-icons**
    >文件的图标生动化，可以在目录中快速辨认文件
    >
    >**使用方式：启动自动调用**
  - **Material Icon Theme**
    >配合上面使用，更多的icon主题
    >
    >**使用方式：启动自动调用，可以通过F1来选择样式**
  - **GitLens**
    >真的是git放大镜，很方便查看日志，比较
    >
    >**使用方式：启动自动调用,左边栏会出现gitlens图标**
  - **Git History**
    >图形化显示日志
    >
    >**使用方式：F1，然后输入git history选择命令**

## 2.2. Markdown

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
  >流程图支持，有Markdown preview enhanced，这个插件可以不装
- **Mermaid Preview**
  >流程图预览支持，有Markdown preview enhanced，这个插件可以不装
- **Markdown TOC**
  >生成目录工具
- **Markdown+Math**
  >数学公式编辑
- **Markdown PDF**
  >markdown转换为pdf/html/jpg/png的工具
- **vscode-pdf**
  >显示pdf文件

## 2.3. 思维导图

- **mindmap**
  >简单的思维导图，写文档的时候可以画一些思路，然后存成图片，导入github等图床

## 2.4. 配置

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
- **多行缩进**
  > tab缩进，shit+tab减少缩进
- **结合git使用**
  >F1，然后输入git，选择相关命令

# 4. debug

## 4.1. python

Debug菜单——>左下角选择好python的编译器,然后可以进行local或者remote的debug，
remote debug需要ptvsd的支持。

`Enjoy it！`