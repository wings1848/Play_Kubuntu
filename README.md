# Kubuntu折腾之旅
记录一下kubuntu用做日常使用的折腾之路，对于其他debian系Linux系统的日常使用有一定参考价值

因为个人的笔记本是很老旧的机子，使用windows10或者11系统会非常卡，于是就想日常改为使用linux内核的系统，先是尝试了arch系的manjaro系统，但折腾中出现了一些无法解决的问题，从台式机上就没有出那样的问题，大概是机子太旧了的原因，就转去折腾kubuntu系统了。

下载kubuntu    https://kubuntu.org/getkubuntu/

下载安装完成kubuntu之后，因为ubuntu自带apt软件包管理器的软件源默认是国外源，为提升软件下载速度，需要修改为国内软件源。

使用命令sudo vim /etc/apt/sources.list使用vim编辑器进入sources.list文件进行编辑，如果提示vim就先使用命令sudo apt-get install vim来安装vim

vim进入sources.list文件后，按i键进行输入如下内容

