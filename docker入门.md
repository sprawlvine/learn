
# 1. 下载软件  
---  
virtualbox最新版本  
debian最新版本，可以直接下一个netinst版本，然后在线安装  
  
# 2. 安装virtual box  
---  
## 2.1 安装增强功能失败  
Q: 提示：未能加载虚拟光盘 C:\Program Files\Oracle\VirtualBox\VBoxGuestAdditions  
A: 可以到系统中的cdrom(注意不是cdrom0，0是只读的，无法直接执行)中，手工执行。  
  
## 2.2 设置剪切板不生效  
A: 需要设置：  
1.虚拟机设置-存储-控制器SATA-勾选"使用主机输入输出(I/O)缓存"  
2.存储-控制器SATA-点击***.vdi-勾选"固态驱动器"  
3.然后重启  
  
## 2.3 共享文件夹无访问权限  
A: 设置：usermod -a -G vboxsf xxx，然后重启  
  
## 2.4 VI箭头输入无效，显示ABCD  
A: sudo apt-get install vim  
  
# 3.安装debian  
---  
磁盘分配建议30G+  
建议所有东西放一个磁盘，或者home分开，但要留够空间给系统，以免安装东西多时系统空间不够  
安装gnome桌面  
安装的时候软件源选择tsing-hua或者163，实际用起来感觉163快  
  
# 4. debian系统初始设置  
---  
terminal放桌面，打开调整color配色  
  
su 以root登录  
  
apt-get update  
apt-get dist-upgrade  
apt-get upgrade  
  
apt-get install sudo  
  
visudo：  
your_user_name ALL=(ALL) NOPASSWD: ALL  
  
# 5. 安装docker  
去docker网站找install guide  
  
添加用户到docker组  
sudo usermod -a -G docker vincent  
重启  
  
# 6. Docker入门与实践  
[Docker入门与实践](https://github.com/yeasy/docker_practice)  
<img src="https://raw.githubusercontent.com/yeasy/docker_practice/master/_images/docker_primer3.png" width = "20%" height = "20%" alt="Docker入门与实践"/>  
  
## 6.1 容器写入操作  
按照 Docker 最佳实践的要求，容器不应该向其存储层内写入任何数据，容器存储  
层要保持无状态化。所有的文件写入操作，都应该使用 数据卷（Volume）、或者  
绑定宿主目录，在这些位置的读写会跳过容器存储层，直接对宿主（或网络存储）  
发生读写，其性能和稳定性更高。  
数据卷的生存周期独立于容器，容器消亡，数据卷不会消亡。因此，使用数据卷  
后，容器删除或者重新运行之后，数据却不会丢失。  
  
## 6.2 Registry  
最常使用的 Registry 公开服务是官方的 Docker Hub，这也是默认的 Registry，并  
拥有大量的高质量的官方镜像。除此以外，还有 CoreOS 的 Quay.io，CoreOS 相  
关的镜像存储在这里；Google 的 Google Container Registry，Kubernetes 的镜像  
使用的就是这个服务。  
  
除了使用公开服务外，用户还可以在本地搭建私有 Docker Registry。Docker 官方  
提供了 Docker Registry 镜像，可以直接使用做为私有 Registry 服务。  
  
  
## 6.3 配置国内镜像加速  
鉴于国内网络问题，后续拉取 Docker 镜像十分缓慢，强烈建议安装 Docker 之后配置国内镜像加速  
  
## 6.4 Docker存储驱动之总览  
+ **Docker的存储驱动架构**  
Docker的存储驱动架构是可插拔的，可以让你很方便的将适合你环境和用例的存储驱动“插进”Docker。每个Docker存储驱动都建立在一种Linux文件系统或者卷管理系统之上，也可以很自由地按照其自己的方法去实现镜像层和容器层的管理。也就是说一些存储驱动在不同的场景下会比其他的驱动性能更好。  
+ **查看当前daemon**  
可以通过docker info命令来查看当前daemon使用着哪种存储驱动。  
<table>  
<tr>  
<th>Storage driver</th> <th>后端文件系统</th> <th>不支持的后端文件系统</th>  
</tr>  
<tr>  
<td>overlay</td> <td>ext4 xfs</td> <td>btrfs aufs overlay zfs eCryptfs</td>  
</tr>  
<tr>  
<td>overlay2</td> <td>ext4 xfs</td> <td>btrfs aufs overlay zfs eCryptfs</td>  
</tr>  
<tr>  
<td>aufs</td> <td>ext4 xfs</td> <td>btrfs aufs eCryptfs</td>  
</tr>  
<tr>  
<td>btrfs</td> <td>btrfs only</td> <td>N/A</td>  
</tr>  
<tr>  
<td>devicemapper</td> <td>direct-lvm</td> <td>N/A</td>  
</tr>  
<tr>  
<td>vfs</td> <td>debugging only</td> <td> N/A</td>  
</tr>  
<tr>  
<td>zfs</td> <td>zfs only</td> <td>N/A</td>  
</tr>  
</table>  
+ **设置**  
+ 启动时设置  
想要设置存储驱动，可以在dockerd启动的时候加入--storage-driver=  
$ dockerd --storage-driver=devicemapper &  
  
+ **Overlay vs Overlay2**  
OverlayFS是一种类似于AUFS的现代联合文件系统，兼容AUFS，具有以下特点：  
.设计简单  
.自3.18版本以来，并入到Linux主线内核  
.性能更优  
基于以上的特点，OverlayFS在Docker社区获得了快速的发展，被很多人看作是AUFS的下一代产品。当然，它现在还仍然年轻，引入到生产环境需要谨慎。  
  
Docker的overlay存储驱动平衡了OverlayFS的多项特性，创建和管理镜像和容器的磁盘结构。  
自1.12版本开始，Docker还提供overlay2存储驱动，在inode利用率上比overlay更有效率，overlay2驱动仅兼容Linux 4.0及其以后的内核。  
  
overlay2驱动程序本身最多支持128个较低的OverlayFS层:  
使用overlay和overlay2驱动性能好于aufs和devicemapper，在实际生产环境overlay2的性能高于btrfs，所以建议使用overlay2.  
  
![overlay原理](https://img-blog.csdn.net/20180131125020902?/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvdTAxMDI3ODkyMw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)  
  
## 6.5 docker 连接  
+ docker attach  
+ nsenter  
管理多个容器很方便  
[nsenter安装使用](https://www.tuicool.com/articles/eYnUBrR)  
  
## 6.6 docker 保存和加载  
+ docker save/load  
+ docker export/import  
*注：*  
---  
用户既可以使用 docker load 来导入镜像存储文件到本地镜像库，也可以使用 docker import 来导入一个容器快照到本地镜像库。这两者的区别在于容器快照文件将丢弃所有的历史记录和元数据信息（即仅保存容器当时的快照状态），而镜像存储文件将保存完整记录，体积也要大。此外，从容器快照文件导入时可以重新指定标签等元数据信息。  
  
## 6.7 docker inspect  
技巧：使用jq解析（apt install jq）  
docker inspect centos|jq '.[].RootFS

<script src="[raphael-min.js](https://raw.githubusercontent.com/DmitryBaranovskiy/raphael/master/raphael.min.js)"><
<script src="[flowchart-latest.js](http://flowchart.js.org/flowchart-latest.js)"></script>


st=>start: Start|past:>http://www.google.com[blank]
e=>end: End|future:>http://www.google.com
op1=>operation: My Operation|past
op2=>operation: Stuff|current
sub1=>subroutine: My Subroutine|invalid
cond=>condition: Yes
or No?|approved:>http://www.google.com
c2=>condition: Good idea|rejected
io=>inputoutput: catch something...|future

st->op1(right)->cond
cond(yes, right)->c2
cond(no)->sub1(left)->op1
c2(yes)->io->e
c2(no)->op2->e
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTc2NDQ2MzkyNCwxNzY0NDYzOTI0LC00OD
QxMzc2OTMsLTgwMTI2NzU2N119
-->