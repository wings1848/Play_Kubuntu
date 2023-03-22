# Kubuntu折腾之旅

## 记录一下kubuntu用做日常使用的折腾之路，对于其他debian系Linux系统的日常使用有一定参考价值

因为个人的笔记本是很老旧的机子，使用windows10或者11系统会非常卡，于是就想日常改为使用linux内核的系统，先是尝试了arch系的manjaro系统，但折腾中出现了一些无法解决的问题，从台式机上就没有出那样的问题，大概是机子太旧了的原因，就转去折腾kubuntu系统了。

## 下载kubuntu

<https://kubuntu.org/getkubuntu/>

## 配置apt软件源

下载安装完成kubuntu之后，因为ubuntu自带apt软件包管理器的软件源默认是国外源，为提升软件下载速度，需要修改为国内软件源。

使用命令```sudo vim /etc/apt/sources.list```使用vim编辑器进入sources.list文件进行编辑，如果提示vim就先使用命令```sudo apt-get install vim```来安装vim

vim进入sources.list文件后，按i键进行复制粘贴输入如下内容

```deb <https://mirrors.bfsu.edu.cn/ubuntu/> jammy main restricted universe multiverse
deb https://mirrors.bfsu.edu.cn/ubuntu/ jammy-updates main restricted universe multiverse
deb https://mirrors.bfsu.edu.cn/ubuntu/ jammy-backports main restricted universe multiverse
deb https://mirrors.bfsu.edu.cn/ubuntu/ jammy-security main restricted universe multiverse
deb http://security.ubuntu.com/ubuntu/ jammy-security main restricted universe multiverse
```

然后按Esc退出编辑模式，按住Shift+：，输入小写字母wq，回车执行，正常的话自动退回到终端

## 更新apt软件源和软件

配置完软件源后，输入命令```sudo apt-get update```更新软件源，再输入命令```sudo apt-get upgrade```更新所有软件

## 添加铜豌豆Linux软件库

铜豌豆软件库官网<https://www.atzlinux.com/allpackages.htm>

添加铜豌豆软件库，方便安装一些日常常用软件，请逐行运行以下命令

```sudo apt-get install wget -y

sudo wget -c -O atzlinux-v11-archive-keyring_lastest_all.deb https://www.atzlinux.com/archive/pool/main/a/atzlinux-keyring/atzlinux-v11-archive-keyring_lastest_all.deb

sudo apt-get install ./atzlinux-v11-archive-keyring_lastest_all.deb -y

sudo apt-get update

sudo apt-get upgrade
```

## 安装日常常用软件命令

安装fcitx5输入法框架```sudo apt-get install fcitx5 -y```

安装搜狗输入法```sudo apt-get install sogoupinyin```
安装输入法之后需要重启电脑，再手动从右下角fcitx5输入法管理器里设置一下顺序

安装软件使用```sudo apt-get install```空格后加上软件包名

安装QQ```sudo apt-get install linuxqq```

安装腾讯会议```sudo apt-get install wemeet```

安装哔哩哔哩```io.github.msojoces.bilibili```

安装网易云音乐替代品```yesplaymusic```

安装迅雷下崽器```com.xunlei.download```

安装百度龟速网盘```baidunetdisk```

安装vs code编辑器```code```

安装微信```electronic-wechat```

安装钉钉```com.alibabainc.dingtalk```

QQ音乐```qqmusic```

腾讯视频```tenvideo-universal```

wps办公```wps-office```

zoom视频会议```zoom```

磁盘管理工具```gparted```